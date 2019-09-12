# Android

Data Binding Basics - https://codelabs.developers.google.com/codelabs/kotlin-android-training-data-binding-basics/index.html


Define Navigation Paths - https://codelabs.developers.google.com/codelabs/kotlin-android-training-add-navigation/index.html

> Navigation destinations are fragments, activities, or other app components that the user navigates to. A navigation graph defines the possible paths from one navigation destination to the next.

> A navigation host fragment, usually named NavHostFragment, acts as a host for the fragments in the navigation graph.

Start an External Activity - https://codelabs.developers.google.com/codelabs/kotlin-android-training-start-external-activity/index.html

> To help catch errors caused by missing keys or mis-matched types when you pass data from one fragment to another, use a Gradle plugin called _Safe Args_.

> An implicit intent declares an action that your app wants some other app (such as a camera app or email app) to perform on its behalf.

> To add an options menu to a fragment, set the `setHasOptionsMenu()` method to `true` in the fragment code.

Lifecycles and Logging - https://codelabs.developers.google.com/codelabs/kotlin-android-training-lifecycles-logging/index.html

> Every activity and every fragment has what is known as a _lifecycle_.

> The `onCreate()` method is where you should do any one-time initializations for your activity.

> The `onCreate()` method is an override, so within it, you must immediately call `super.onCreate()`. The same is true for other lifecycle methods.

ViewModel and ViewModel Factory - https://codelabs.developers.google.com/codelabs/kotlin-android-training-view-model/index.html

> _ViewModel_ and _LiveData_ are Android Architecture Components, which are libraries and other components that help you design robust, testable, maintainable apps.

> App architecture is a way of designing your apps' classes, and the relationships between them, such that the code is organized, performs well in particular scenarios, and is easy to work with.

> A `ViewModel` holds data to be displayed in a fragment or activity associated with the `ViewModel`. 

> Right before the ViewModel is destroyed, the `onCleared()` callback is called to clean up the resources.

> A _factory method_ is a method that returns an instance of the same class.

LiveData and LiveData Observers - https://codelabs.developers.google.com/codelabs/kotlin-android-training-live-data/index.html

> LiveData, which is one of the Android Architecture Components, lets you build data objects that notify views when the underlying database changes.

> Data in a MutableLiveData object can be changed, as the name implies. Inside the ViewModel, the data should be editable, so it uses MutableLiveData.

> Data in a LiveData object can be read, but not changed. From outside the ViewModel, data should be readable, but not editable, so the data should be exposed as LiveData.

Data binding with ViewModel and LiveData - https://codelabs.developers.google.com/codelabs/kotlin-android-training-live-data-data-binding/index.html

> _Listener bindings_ are binding expressions that run when events such as onClick(), onZoomIn(), or onZoomOut() are triggered. Listener bindings are written as lambda expressions.

> Listener bindings work with the Android Gradle Plugin version 2.0 or higher.

LiveData Transformations - https://codelabs.developers.google.com/codelabs/kotlin-android-training-live-data-transformations/index.html

Room Database - https://codelabs.developers.google.com/codelabs/kotlin-android-training-room-database/index.html

> Room is a database library that's part of Android Jetpack. 

> Room is an abstraction layer on top of an SQLite database.

> You must define each entity as an annotated data class, and the interactions as an annotated interface, a data access object (DAO). Room uses these annotated classes to create tables in the database, and queries that act on the database.

Build your first app - https://developer.android.com/training/basics/firstapp/

Android apps are built as a combination of components that can be invoked individually. For example, an activity is a type of app component that provides a user interface (UI).

Android apps provide multiple entry points. The "main" activity starts when the user taps your app's icon. You can also direct the user to an activity from elsewhere, such as from a notification or even from a different app.

Other components, such as _broadcast receivers_ and _services_, allow your app to perform background tasks without a UI.

Android apps adapt to different devices.

Android allows you to provide different resources for different devices. For example, you can create different layouts for different screen sizes. The system determines which layout to use based on the screen size of the current device.

If any of your app's features need specific hardware, such as a camera, you can query at runtime whether the device has that hardware or not, and then disable the corresponding features if it doesn't. You can specify that your app requires certain hardware so that Google Play won't allow the app to be installed on devices without them.


