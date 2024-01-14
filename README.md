# Android-RoadMap-1 `v1.0.0-alpha01`

Androidv14 - Level34

# APP ARCHITECTURE - Basics

# **1. App Entry Points**

## **1.1 ACTIVITIES**

### **1.1.1 Introduction to activities**

- The concept of activities
- Configuring the manifest
    - Declare activities
    - Declare intent filters
    - Declare permissions
- Managing the activity lifecycle
    - onCreate()
    - onStart()
    - onResume()
    - onPause()
    - onStop()
    - onRestart()
    - onDestroy()
 
### **1.1.2 The activity lifecycle**

- Activity-lifecycle concepts
- Lifecycle callbacks
    - onCreate()
    - onStart()
    - onResume()
    - onPause()
    - onStop()
    - onRestart()
    - onDestroy()
- Activity state and ejection from memory
- Saving and restoring transient UI state
    - Instance state
    - Save simple, lightweight UI state using onSaveInstanceState()
    - Restore activity UI state using saved instance state
- Navigating between activities
    - Starting one activity from another
 
### **1.1.3 Activity state changes**

- Configuration change occurs
    - Handle multi-window cases
- Activity or dialog appears in foreground
- User taps or gestures Back
- System kills app process

### **1.1.4 Test your app's activities**

- Drive an activity's state
    - Create an activity
    - Drive the activity to a new state
    - Determine the current activity state
    - Recreate the activity
    - Retrieve activity results
    - Trigger actions in the activity

### **1.1.5 Tasks and the back stack**

- Lifecycle of a task and its back stack
    - Back tap behavior for root launcher activities
    - Background and foreground tasks
    - Multiple activity instances
    - Multi-window environments
    - Lifecycle recap
- Manage tasks
    - Define launch modes
    - Handle affinities
    - Clear the back stack
    - Start a task

### **1.1.6 Processes and app lifecycle**

### **1.1.7 Parcelables and bundles**

- Sending data between activities
- Sending data between processes

### **1.1.8 Loaders**

- Loader API summary
- Use loaders in an application
    - Start a loader
    - Restart a loader
    - Use the LoaderManager callbacks
- Example

### **1.1.9 Recents screen**

- Add tasks to the Recents screen
    - Use the Intent flag to add a task
    - Use the activity attribute to add a task
- Remove tasks
    - Use the AppTask class to remove tasks
    - Retain finished tasks
- Enable recents URL sharing (Pixel only)

### **1.1.10 Restrictions on starting activities from the background**

- Display notifications instead
- When apps can start activities

## **1.2 APP SHORTCUTS**

### **1.2.1 About Shortcut**

- Shortcut types
- Display shortcuts in assistants using capabilities
- Shortcut limitations

### **1.2.2 Create shortcuts**

- Create static shortcuts
    - Customize attribute values
    - Configure inner elements
- Create dynamic shortcuts
    - Add the Google Shortcuts Integration Library
- Create pinned shortcuts
    - Create a custom shortcut activity
- Test shortcuts

### **1.2.3 Add capabilities to shortcuts**

- Define capabilities in shortcuts.xml
- Associate shortcuts with a capability

### **1.2.4 Manage shortcuts**

- Shortcut behavior
    - Shortcut visibility
    - Shortcut display order
- Manage multiple intents and activities
    - Assign multiple intents
    - Start one activity from another
    - Set intent flags
- Update shortcuts
    - Handle system locale changes
    - Track shortcut usage
- Disable shortcuts
- Rate limiting
- Backup and restore

### **1.2.5 Best practices for shortcuts**

- Follow the design guidelines
- Publish only four distinct shortcuts
- Limit shortcut description length
- Maintain shortcut and action usage history
- Update shortcuts only when their meaning is retained
- Check dynamic shortcuts whenever you launch your app

===========================================================================

# **2. App Navigation**

### **2.1 Principles of navigation**

- Fixed start destination
- Navigation state is represented as a stack of destinations
- Up and Back are identical within your app's task
- The Up button never exits your app
- Deep linking simulates manual navigation

## **2.2 FRAGMENTS**

### **2.2.1 About Fragments**

- Fragments
- Modularity

### **2.2.2 Create a fragment**

- Setup your environment
- Create a fragment class
- Add a fragment to an activity
    - Add a fragment via XML
    - Add a fragment via XML

### **2.2.3 Fragment manager**

- Access the FragmentManager
    - Child fragments
- Use the FragmentManager
- Perform a transaction
    - Find an existing fragment
    - Special considerations for child and sibling fragments
- Support multiple back stacks
- Provide dependencies to your fragments
    - Test with FragmentFactory

### **2.2.4 Fragment transactions**

- Allow reordering of fragment state changes
- Adding and removing fragments
    - Commit is asynchronous
    - Operation ordering is significant
- Limit the fragment's lifecycle
- Showing and hiding fragment's views
- Attaching and detaching fragments

### **2.2.5 Navigate between fragments using animations**

- Set animations
- Set transitions
- Use shared element transitions
- Postponing transitions
- Use shared element transitions with a RecyclerView

### **2.2.6 Fragment lifecycle**

- Fragments and the fragment manager
- Fragment lifecycle states and callbacks
    - Upward state transitions
    - Downward state transitions

### **2.2.7 Saving state with fragments**

- View state
- SavedState
- NonConfig

### **2.2.8 Communicate with fragments**

- Share data using a ViewModel
    - Share data with the host activity
    - Share data between fragments
- Get results using the Fragment Result API
    - Pass results between fragments
    - Pass results between parent and child fragments
    - Receive results in the host activity

### **2.2.9 Working with the AppBar**

- Activity-owned app bar
    - Register with activity
    - Inflate the menu
    - Handle click events
    - Dynamically modify the menu
- Fragment-owned app bar
    - Inflate the menu
    - Handle click events
    - Dynamically modify the menu
    - Add a navigation icon
 
### **2.2.10 Display dialogs with DialogFragment**

- Create a DialogFragment
- Show the DialogFragment
- DialogFragment lifecycle
- Use custom views

### **2.2.11 Debug your fragments**

- FragmentManager logging
    - DEBUG logging
    - VERBOSE logging
- StrictMode for fragments
    - Fragment reuse
    - Fragment tag usage
    - Retain instance usage
    - Set user visible hint
    - Target fragment usage
    - Wrong fragment container

### **2.2.12 Test your fragments**

- Declaring dependencies
- Create a fragment
- Provide dependencies
- Drive the fragment to a new state
- Recreate the fragment
- Interacting with UI fragments
- Test dialog actions


## **2.3 Navigation Component**

### **2.3.1 Navigation Overview**

- Key concepts
- Benefits and features
- Set up your environment

### **2.3.2 Navigation Controller**

- Create a navigation controller
- Compose
- Views

## ****2.3.3 Design Your Navigation Graph****

### **2.3.3.1 Navigation Graph Overview**

- Destination types
    - Frameworks
- Compose
    - Minimal example
- Fragments
    - Programmatically
    - XML
    - Editor
- Nested graphs

### **2.3.3.2 Dialog destinations**

- Dialog composable
- Kotlin DSL
- XML

### **2.3.3.3 Activity destinations**

- Compose and Kotlin DSL
- XML
- Dynamic arguments

### **2.3.3.4 Nested graphs**

- Example
- Compose
    - Extension functions
- XML
    - Reference other navigation graphs with include

### **2.3.3.5 Deeplinks**

- Create a deep link for a destination
- Create an explicit deep link
- Create an implicit deep link
- Handling deep links

### **2.3.3.6 New destination types**

### **2.3.3.7 Type safety in Kotlin DSL and Navigation Compose**

- Split your navigation graph
- Type safe navigation
    - Navigate to a destination
    - Type safe arguments wrapper
- Assemble the navigation graph
- Type safety in nested navigation graphs

### **2.3.3.8 Global Actions**

- Use Navigation actions and Fragments
- Examples
    - Navigate using an action
- Global actions

### **2.3.3.9 Build a graph programmatically using the Kotlin DSL**

- Dependencies
- Building a graph
    - Hosting a Kotlin DSL Nav Graph
    - Create constants for your graph
    - Build a graph with the NavGraphBuilder DSL
    - Navigating with your Kotlin DSL graph
- Destinations
    - Fragment destinations
    - Activity destination
    - Navigation graph destination
    - Supporting custom destinations
    - Providing destination arguments
- Deep links
- Limitations

### **2.3.3.10 Navigation Editor**

- Overview
- Add destinations
    - Create a destination from an existing fragment or activity
    - Create a new fragment destination
    - Anatomy of a destination
- NavHostFragment
- Connect destinations
- Placeholder destinations

## ****2.3.4 Use Your Navigation Graph****

### **2.3.4.1 Navigate to a destination**

- Use a NavController
- Navigate
- Navigate to a composable
    - Expose events from your composables
- Navigate using integer ID
- Navigate using plinkrepLinkRequest
    - Actions and MIME types

### **2.3.4.2 Navigate with options**

- Options with Compose
- Options with XML
    - Apply options programmatically

### **2.3.4.3 Safe Args**

- Enable Safe Args
- Generated code
- Safe Args example
- Ensure type safety by using Safe Args

### **2.3.4.4 Pass data between destinations**

- Define destination arguments
    - Supported argument types
    - Override a destination argument in an action
- Use Safe Args to pass data with type safety
    - Use Safe Args with a global action
- Pass data between destinations with Bundle objects
- Pass data to the start destination
- ProGuard considerations
    - Use @Keep annotations
    - Use keepnames rules

### **2.3.4.5 Animate transitions between destinations**

- Add shared element transitions between destinations
    - Shared element transitions to a fragment destination
    - Shared element transitions to an activity destination
- Apply pop animations to activity transitions

### **2.3.4.6 Conditional navigation**

- User login

### **2.3.4.7 Interact programmatically with the Navigation component**

- Create a NavHostFragment
- Reference a destination using NavBackStackEntry
- Returning a result to the previous Destination
    - Considerations when using dialog destinations
- Share UI-related data between destinations with ViewModel
- Modifying inflated navigation graphs

## ****2.3.5 The Back Stack****

### **2.3.5.1 Overview**

- Basic behavior
- Pop back
    - Pop back to a particular destination
    - Handle a failed pop back
- Pop up to a destination
    - Save state when popping up
    - XML example
    - Compose Examples
- Pop using actions

### **2.3.5.2 Dialogs and the back stack**

- Overview
- Example

### **2.3.5.3 Circular navigation and  the back stack**

- Scenario
- Solution
    - Compose implementation
    - Views implementation

### **2.3.5.4 Multiple back stacks**

- Implement support automatically with NavigationUI
- Implement support manually with underlying APIs
    - Navigation XML
    - NavOptions

## ****2.3.6 Integration****

### **2.3.6.1 Navigate with feature modules**

- Setup
- Basic usage
- Customize the progress fragment
- Monitor the request state
- Included graphs
    - Use the correct graphPackage
    - Navigating to an include-dynamic navigation graph
- Limitations

### **2.3.6.2 Multi-module projects**

- The role of the `app` module
- Navigation best practices for multi-module projects
- Navigating across feature modules

### **2.3.6.3 Connect UI components to NavController using NavigationUI**

- Top app bar
    - AppBarConfiguration
    - Create a Toolbar
    - Include CollapsingToolbarLayout
    - Action bar
    - Support app bar variations
- Tie destinations to menu items
- Add a navigation drawer
- Bottom navigation
- Listen for navigation events
    - Argument-based listeners

### **2.3.7 Migrate to the Navigation Component**

- Prerequisites
- Move screen-specific UI logic out of activities
    - Introducing fragments
    - Create a New Layout to Host the UI
    - Create a fragment
    - Move activity logic into a fragment
    - Initialize the fragment in the host activity
    - Pass intent extras to the fragment
- Integrate the Navigation component
    - Create a navigation graph
    - Remove fragment transactions
- Add activity destinations
    - Pass activity destination args to a start destination fragment
- Combine activities

### **2.3.8 Test Navigation**

- Test fragment navigation
- Test NavigationUI with FragmentScenario
- Testing interactions with back stack entries

## **2.4 Custom Back Navigation**

- Implement custom back navigation
- Activity onBackPressed()

### **2.4.1 Predictive back gesture**

- Update an app that uses default back navigation
- Update an app that uses custom back navigation
    - Migrate an AndroidX back navigation implementation
    - Migrate an AndroidX app containing unsupported back navigation APIs to AndroidX APIs
    - Migrate an app that uses unsupported back navigation APIs to platform APIs
- Opt-in to the predictive back gesture
    - Opt-in at an activity level
- Callback best practices
    - Determine the UI State that enables and disables each callback
    - Use system back callbacks for UI Logic
    - Create single responsibility callbacks
- Test the predictive back gesture animation

### **2.4.2 Add support for predictive back animations**

- Add custom in-app transitions and animations
    - Add custom transitions using the Progress API
    - Add custom activity transitions on Android 14 and higher
    - Add support for Predictive Back with fragments
- Requirements

## **2.5 Responsive Design**

### **2.5.1 Handling configuration changes**

- Responsive UI and navigation
- Implementing global navigation in a responsive UI
- Consider alternatives to split-view layouts
- Destination names

### **2.5.2 Design for different form factors**

- Designing responsive content
- Providing tailored user experiences

## **2.6 Swipe Between Views**

### **2.6.1 Create swipe views with tabs using ViewPager2**

- Implement Swipe Views
- Add Tabs Using a TabLayout

### **2.6.2 Create swipe views with tabs using ViewPager**

- Implement swipe views
- Add tabs using a TabLayout

## **2.7 App Links**

### **2.7.1 About App Links**

- Understand the different types of links
    - Deep links
    - Web links
    - Android App Links
- Add Android App Links
- Manage and verify Android App Links

### **2.7.2 Create Deep Links to App Content**

- Add intent filters for incoming links
- Read data from incoming intents
- Test your deep links

### **2.7.3 Verify Android App Links**

- Add intent filters for app links verification
    - Supporting app linking for multiple hosts
    - Supporting app linking for multiple subdomains
    - Supporting app linking for multiple subdomains
- Declare website associations
    - Associating a website with multiple apps
    - Associating multiple websites with a single app
    - Publishing the JSON verification file
- Android App Links verification
    - Auto verification
    - Manual verification
- Request the user to associate your app with a domain
    - Check whether your app is already approved for the domain
    - Provide context for the request
    - Make the request
- Open domains in your app that your app cannot verify
- Test app links
    - Confirm the list of hosts to verify
    - Confirm the Digital Asset Links files
    - Check link policies
    - Test example
- Fix common implementation errors

## **2.7.4 Create App Links for Instant Apps**

- App links overview
- How app links for instant apps are different
- Other reminders when creating app links

## **2.8 Interact with other apps**

### **2.8.1 About Interact with other apps**

### **2.8.2 Intents and intent filters**

- Intent types
- Building an intent
    - Example explicit intent
    - Example implicit intent
    - Forcing an app chooser
    - Detect unsafe intent launches
- Receiving an implicit intent
    - Example filters
- Match intents to other apps' intent filters
- Using a pending intent
    - Specify mutability
    - Use explicit intents within pending intents
- Intent resolution
    - Action test
    - Category test
    - Data test
    - Intent matching

### **2.8.3 Common intents**

- Alarm clock
    - Create an alarm
    - Create a timer
    - Show all alarms
- Calendar
    - Add a calendar event
- Camera
    - Capture a picture or video and return it
    - Start a camera app in still image mode
    - Start a camera app in video mode
- Contacts/people app
    - Select a contact
    - Select specific contact data
    - View a contact
    - Edit an existing contact
    - Insert a contact
- Email
    - Compose an email with optional attachments
- File storage
    - Retrieve a specific type of file
    - Open a specific type of file
- Local actions
    - Call a car
- Maps
    - Show a location on a map
- Music or video
    - Play a media file
    - Play music based on a search query
- New note
    - Create a note
- Phone
    - Initiate a phone call
- Search
    - Search using a specific app
    - Perform a web search
- Settings
- Text messaging
    - Compose an SMS/MMS message with attachment
- Web browser
    - Load a web URL
- Verify intents with the Android Debug Bridge

### **2.8.4 Sending the user to another app**

- Build an implicit intent
    - Associate intent actions with data
    - Add extras to an intent
- Start an activity with the intent
    - Handle the situation where no app can receive an intent
    - Disambiguation dialog
    - Complete example
- Show an app chooser

### **2.8.5 Get a result from an activity**

- Register a callback for an activity result
- Launch an activity for result
- Receive an activity result in a separate class
- Test
- Create a custom contract

### **2.8.6 Let other apps start your activity**

- Add an intent filter
- Handle the intent in your activity
- Return a result

### **2.8.7 Limit loading in on-device Android containers**

## ****2.8.8 Package visibility****

### **2.8.8.1 About Package visibility**

### **2.8.8.2 Know which packages are visible automatically**

- Types of apps that are visible automatically
- System packages that are visible automatically

### **2.8.8.3 Declare package visibility needs**

- Specific package names
    - Communicate with a host app in a library
- Packages that match an intent filter signature
- Packages that use a specific authority
- All apps (not recommended)

### **2.8.8.4 Fulfill common use cases while having limited package visibility**

- Open URLs
    - Open URLs in a browser or other app
    - Open URLs in Custom Tabs
    - Let non-browser apps handle URLs
    - Avoid a disambiguation dialog
- Open a file
    - Grant URI access
- Connect to services
    - Connect to a text-to-speech engine
    - Connect to a speech recognition service
    - Connect to media browser services
- Provide custom functionality
    - Query for SMS apps
    - Create a custom sharesheet
    - Show custom text selection actions
    - Show custom data rows for a contact

### **2.8.8.5 Test package visibility behavior**

- Test the behavior changes
- Configure log messages for package filtering

===========================================================================

# **3. Dependency Injection**

### **3.1 Dependency injection**

- Fundamentals of dependency injection
    - What is dependency injection?
    - Automated dependency injection
- Alternatives to dependency injection
- Use Hilt in your Android app

### **3.2 Manual dependency injection**

- Basics of manual dependency injection
- Managing dependencies with a container
- Managing dependencies in application flows

### **3.3 Dependency injection with Hilt**

- Adding dependencies
- Hilt application class
- Inject dependencies into Android classes
- Define Hilt bindings
- Hilt modules
    - Inject interface instances with @Binds
    - Inject instances with @Provides
    - Provide multiple bindings for the same type
    - Predefined qualifiers in Hilt
- Generated components for Android classes
    - Component lifetimes
    - Component scopes
    - Component hierarchy
    - Component default bindings
- Inject dependencies in classes not supported by Hilt
- Hilt and Dagger

### **3.4 Hilt in multi-module apps**

- Hilt in feature modules

### **3.5 Use Hilt with other Jetpack libraries**

- **Inject ViewModel objects with Hilt**
    - **@ViewModelScoped**
- **Integration with the Jetpack navigation library**
- **Integration with Jetpack Compose**
- **Inject WorkManager with Hilt**

### **3.6 Hilt testing guide**

- Unit tests
- End-to-end tests
    - Adding testing dependencies
    - UI test setup
    - Testing features
- Special cases
    - Custom application for tests
    - Multiple TestRule objects in your instrumented test
    - launchFragmentInContainer
    - Use an entry point before the singleton component is available

### **3.7 Hilt and Dagger annotations cheat sheet**

## **3.8 Dagger**

### **3.8.1 Dagger basics**

- Benefits of using Dagger
- A simple use case in Dagger: Generating a factory
- Dagger components
    - Scoping with Dagger

### **3.8.2 Using Dagger in Android apps**

- Best practices summary
- Adding dependencies
- Dagger in Android
    - Injecting activities
    - Dagger modules
    - Dagger scopes
    - Dagger subcomponents
    - Assigning scopes to subcomponents
- Best practices when building a Dagger graph
- Testing a project that uses Dagger
    - Unit tests
    - End-to-end tests
- Working with Dagger modules
- Assisted injection

### **3.8.3 Using Dagger in multi-module apps**

- Implementation with Dagger subcomponents
- Component dependencies with feature modules
- Best practices

===========================================================================

# **4. App Startup**

- Setup
- Initialize components at app startup
    - Implement component initializers
    - Set up manifest entries
    - Run lint checks
- Manually initialize components
    - Disable automatic initialization for an individual component
    - Disable automatic initialization for all components
    - Manually call component initializers
