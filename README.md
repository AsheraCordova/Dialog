# Dialog

Dialog project add support for dialogs.

Important Links:

https://asheracordova.github.io/

https://asheracordova.github.io/doc/help-doc.html

To install the plugin use:
```
cordova plugin add https://github.com/AsheraCordova/Dialog.git
```

## How to create a dialog

The dialog is defined in nav_graph.xml as follows:

```
<dialog
        android:id="@+id/dashboard_filter"
        android:name="com.ashera.core.MyDialog"
        android:label=""
        style="@style/MyDialogStyle"
        tools:layout="@layout/dashboard_filter"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
    </dialog>
```

The following table list important attributes which can be used to configure a dialog:

Name                              | Description
-------------                     | -------------
android:windowCloseOnTouchOutside | When true click on backdrop of the dialog will close the dialog.
backdropColor                     | Color of backdrop.
android:backgroundDimEnabled      | Back drop will be disabled
marginPercent                     | Percentage of margin around the dialog.

Dialog Theming:

The following snippet shows the configuration for different kinds of dialog:
```
      <style name="MyDialogStyle" parent="android:Theme.Dialog" attrs="">
          <item name="android:windowCloseOnTouchOutside">false</item>
      </style>
      <style name="MyDialogStyleCloseOnTouchOutside" parent="android:Theme.Dialog" attrs="">
          <item name="android:windowCloseOnTouchOutside">true</item>
      </style>

      <style name="MyDialogStyleCustomBackDrop" parent="android:Theme.Dialog" attrs="backdropColor:#E6ff0000">
          <item name="android:windowCloseOnTouchOutside">true</item>
      </style>
      <style name="MyDialogBackgroundDimDisabledStyle" parent="android:Theme.Dialog" attrs="">
          <item name="android:windowCloseOnTouchOutside">false</item>
          <item name="android:backgroundDimEnabled">false</item>
      </style>

      <style name="MyDialogFullScreenStyle" parent="Theme.AppCompat.Dialog" attrs="marginPercent:1;">
          <item name="android:backgroundDimEnabled">false</item>
          <item name="android:windowNoTitle" android="true">true</item>
          <item name="android:statusBarColor" android="true">#fff</item>
          <item name="android:windowIsFloating" android="true">false</item>
          <item name="android:windowBackground" android="true">@android:color/white</item>
          <item name="android:windowCloseOnTouchOutside">false</item>
      </style>

```
