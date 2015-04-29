# Keyboard
Working With Keyboard

// Show a keyboard with delay.

	public static void openKeypad(final Context context, final View v) 
	   {
		new Handler().postDelayed(new Runnable() 
		{
			@Override
			public void run() 
			{
				InputMethodManager inputManager = (InputMethodManager)context.getSystemService(Context.INPUT_METHOD_SERVICE); 
				inputManager.showSoftInput(v, InputMethodManager.SHOW_IMPLICIT);	
				Log.e("openKeypad", "Inside Handler");
			}
		},300);
	}
	
	// close Keypad
	
	public static void closeKeyPad(Context context, View v)
    {
		InputMethodManager inputMethodManager = (InputMethodManager)context.getSystemService(Context.INPUT_METHOD_SERVICE);
		inputMethodManager.hideSoftInputFromWindow(v.getWindowToken(), 0);
    }
    
    // to know whether keypad is showing or Not
    
    
