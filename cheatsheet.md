
## LESSON 1: Create Project Sunshine

### 1.9: Setting Min and Target Versions

* minSdk - minimum SDK supported
* targetSdk - the highest SDK version you've tested your app on

### 1.12: Activities, Packages and Layouts

There are 4 components that make up apps:

* Activity
* Service
* Broadcast Receiver
* Content Provider

They are registered in the Android manifest.

An activity is the Android component responsible for most app user interaction.
Activity: **single focused** thing that the user can do.
Responsible for creating the window that your application uses to draw and
receive events from the system.

### 1.14: Android Layouts Primer

An activity creates views to show the user information, and to let the user
interact with the activity.

Views are a class in the Android UI framework. They occupy a rectangular area on
the screen and are responsible for drawing and handling events.

An activity determines what views to create (and where to put them), by reading
an XML layout file. These XML files, as Dan mentioned, are stored in the res
folder inside the folder labeled layouts.

#### UI Components

```
Class Name     Description
--------------------------
TextView       Creates text on the screen; generally non interactive text.
EditText       Creates a text input on the screen
ImageView      Creates an image on the screen
Button         Creates a button on the screen
Chronometer    Create a simple timer on screen
```

```
Class Name         Description
------------------------------
LinearLayout       Displays views in a single column or row.
RelativeLayout     Displays views positioned relative to each other and this
                   view.
FrameLayout        A ViewGroup meant to contain a single child view.
ScrollView         A FrameLayout that is designed to let the user scroll through
                   the content in the view.
ConstraintLayout   This is a newer viewgroup; it positions views in a flexible
                   way.
```

##### wrap_content

It will shrink the view to wrap whatever is displayed inside the view.

##### match_parent

It will expand the size of the view to be as large as the parent view which it
is nested inside of.

#### The R Class

When your application is compiled the R class is generated. It creates constants
that allow you to dynamically identify the various contents of the res folder,
including layouts.

https://developer.android.com/guide/topics/resources/providing-resources#Accessing

#### setContentView

It inflates the layout. Essentially what happens is that Android reads your XML
file and generates Java objects for each of the tags in your layout file.
You can then edit these objects in the Java code by calling methods on the Java
objects.
