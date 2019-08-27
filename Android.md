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
