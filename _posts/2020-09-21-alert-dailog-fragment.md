---
layout: post
title: "Dialog fragment and custom positioning"
comments: true
author: "waliahimanshu"
meta: "Alert dialog in Android"
categories: Android
---


### Alert dialog
Use it when you just want to show a `title`, up to three `buttons`, a list of `selectable items`, or a `custom layout`.

Also `DatePickerDialog` and `TimePickerDialog` are available with a pre-defined android style widgets, that allows the user to select a date or time.

### DialogFragment

Use a DialogFragment as a container for your dialog, when you need  
* to ensures that it correctly handles lifecycle events such as when the user presses the back button or rotates the screen. 
* to allow reuse the dialog's UI just like in a traditional Fragment (such as when you want the dialog UI to appear differently on large and small screens).


```ruby
class FireMissilesDialogFragment : DialogFragment() {

    override fun onCreateDialog(savedInstanceState: Bundle): Dialog {
        return requireActivity()?.let {
            // Use the Builder class for convenient dialog construction
            val builder = AlertDialog.Builder(it)
            builder.setMessage(R.string.dialog_fire_missiles)
                    .setPositiveButton(R.string.fire,
                            DialogInterface.OnClickListener { dialog, id ->
                            })
                    .setNegativeButton(R.string.cancel,
                            DialogInterface.OnClickListener { dialog, id ->
                                // User cancelled the dialog
                            })
            // Create the AlertDialog object and return it
            builder.create()
        } ?: throw IllegalStateException("Activity cannot be null")
    }
} 

// Showing a Dialog

fun confirmFireMissiles() {
    val newFragment = FireMissilesDialogFragment()
    newFragment.show(supportFragmentManager, "missiles")
}

```

The show method add the fragment in transaction and commits,
however you can not pop back this fragment from stack.

```ruby
class CustomDialogFragment : DialogFragment() {

    /** The system calls this to get the DialogFragment's layout, regardless
    of whether it's being displayed as a dialog or an embedded fragment. */
    override fun onCreateView(
            inflater: LayoutInflater,
            container: ViewGroup?,
            savedInstanceState: Bundle?
    ): View {
        // Inflate the layout to use as dialog or embedded fragment
        return inflater.inflate(R.layout.purchase_items, container, false)
    }

    /** The system calls this only when creating the layout in a dialog. */
    override fun onCreateDialog(savedInstanceState: Bundle): Dialog {
        // The only reason you might override this method when using onCreateView() is
        // to modify any dialog characteristics. For example, the dialog includes a
        // title by default, but your custom layout might not need it. So here you can
        // remove the dialog title, but you must call the superclass to get the Dialog.
        val dialog = super.onCreateDialog(savedInstanceState)
        dialog.requestWindowFeature(Window.FEATURE_NO_TITLE)
        return dialog
    }
}
```


```ruby
fun showDialog() {
    val fragmentManager = supportFragmentManager
    val newFragment = CustomDialogFragment()
    if (isLargeLayout) {
        // The device is using a large layout, so show the fragment as a dialog
        newFragment.show(fragmentManager, "dialog")
    } else {
        // The device is smaller, so show the fragment fullscreen
        val transaction = fragmentManager.beginTransaction()
        // For a little polish, specify a transition animation
        transaction.setTransition(FragmentTransaction.TRANSIT_FRAGMENT_OPEN)
        // To make it fullscreen, use the 'content' root view as the container
        // for the fragment, which is always the root view for the activity
        transaction
                .add(android.R.id.content, newFragment)
                .addToBackStack(null)
                .commit()
    }
}
```


### Changing the position of the dialog.
```ruby
    private fun setupDialogProperties(alertDialog: AlertDialog) {
        val OFFSET_IN_PX = 140
        alertDialog.apply {
            window?.let { window ->
                window.setBackgroundDrawableResource(R.drawable.bg_drawable)
                window.setDimAmount(0.1f) // from 0 for no dim to 1 for full dim.
                window.attributes?.let { params ->
                    params.width = WindowManager.LayoutParams.MATCH_PARENT
                    params.height = WindowManager.LayoutParams.WRAP_CONTENT
                    params.gravity = Gravity.TOP or Gravity.CENTER
                    params.y = (OFFSET_IN_PX).toFloat())
                    params.x = 0
                }
            }
            setCanceledOnTouchOutside(true)
            setCancelable(true)
            requestWindowFeature(Window.FEATURE_NO_TITLE)
        }
    }
```