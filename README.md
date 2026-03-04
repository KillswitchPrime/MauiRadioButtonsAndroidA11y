# What is the issue?
Turn on TalkBack in the Android Accessibility settings.
Open the app and see that the different radio button groups behave weirdly.
The first group has `SemanticProperties.Description` added, which makes the screenreader correctly read out the label on the radio button.
But it does not give the user any indication of the current state of the button, whether it is toggled or not.

The second group does not have the `SemanticProperties.Description` property, 
which makes the screenreader announce the actual name of the Maui component instead, ala "Microsoft.Maui.Controls.View".
This is obviously VERY wrong.

The last group is a completely normal radio button without any Content properties, just as basic as possible.
On this group the screenreader works exactly as expected.
