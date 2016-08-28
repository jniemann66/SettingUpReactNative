# Command Reference

### react-native

$ react-native --help

  Usage: index [options] [command]


  Commands:

    start [options]          starts the webserver
    run-ios [options]        builds your app and starts it on iOS simulator
    run-android [options]    builds your app and starts it on a connected Android emulator or device
    new-library [options]    generates a native library bridge
    bundle [options]         builds the javascript bundle for offline use
    unbundle [options]       builds javascript as "unbundle" for offline use
    link [packageName]       links all native dependencies
    unlink <packageName>     unlink native dependency
    install <packageName>    install and link native dependencies
    uninstall <packageName>  uninstall and unlink native dependencies
    upgrade                  upgrade your app's template files to the latest version; run this after updating the react-native version in your package.json and running npm install
    log-android              starts adb logcat
    log-ios                  starts iOS device syslog tail

  Options:

    -h, --help     output usage information
    -V, --version  output the version number

### react-native start

react-native start [options]
  starts the webserver

  Options:

    -h, --help                   output usage information
    --port [number]
    --host [string]
    --root [list]                add another root(s) to be used by the packager in this project
    --projectRoots [list]        override the root(s) to be used by the packager
    --assetRoots [list]          specify the root directories of app assets
    --skipflow                   Disable flow checks
    --nonPersistent              Disable file watcher
    --transformer [string]       Specify a custom transformer to be used (absolute path)
    --reset-cache, --resetCache  Removes cached files
    --verbose                    Enables logging

### react-native bundle

	react-native bundle --platform android --dev true --reset-cache --entry-file index.android.js --bundle-output "AbsolutePathToProject\app\build\intermediates\assets\debug\index.android.bundle" --assets-dest "AbsolutePathToProject\android\app\build\intermediates\res\merged\debug"



### gradlew
$ gradlew.bat --help

USAGE: gradlew [option...] [task...]

	-?, -h, --help          Shows this help message.
	-a, --no-rebuild        Do not rebuild project dependencies.
	-b, --build-file        Specifies the build file.
	-c, --settings-file     Specifies the settings file.
	--configure-on-demand   Only relevant projects are configured in this build run. This means faster build for large multi-project builds. [incubating]
	--console               Specifies which type of console output to generate. Values are 'plain', 'auto' (default) or 'rich'.
	--continue              Continues task execution after a task failure.
	-D, --system-prop       Set system property of the JVM (e.g. -Dmyprop=myvalue).
	-d, --debug             Log in debug mode (includes normal stacktrace).
	--daemon                Uses the Gradle daemon to run the build. Starts the daemon if not running.
	--foreground            Starts the Gradle daemon in the foreground. [incubating]
	-g, --gradle-user-home  Specifies the gradle user home directory.
	--gui                   Launches the Gradle GUI.
	-I, --init-script       Specifies an initialization script.
	-i, --info              Set log level to info.
	-m, --dry-run           Runs the builds with all task actions disabled.
	--max-workers           Configure the number of concurrent workers Gradle is allowed to use. [incubating]
	--no-color              Do not use color in the console output. [deprecated - use --console=plain instead]
	--no-daemon             Do not use the Gradle daemon to run the build.
	--offline               The build should operate without accessing network resources.
	-P, --project-prop      Set project property for the build script (e.g. -Pmyprop=myvalue).
	-p, --project-dir       Specifies the start directory for Gradle. Defaults to current directory.
	--parallel              Build projects in parallel. Gradle will attempt to determine the optimal number of executor threads to use. [incubating]
	--parallel-threads      Build projects in parallel, using the specified number of executor threads. [deprecated - Please use --parallel, optionally in conjunction with --max-workers.] [incubating]
	--profile               Profiles build execution time and generates a report in the <build_dir>/reports/profile directory.
	--project-cache-dir     Specifies the project-specific cache directory. Defaults to .gradle in the root project directory.
	-q, --quiet             Log errors only.
	--recompile-scripts     Force build script recompiling.
	--refresh-dependencies  Refresh the state of dependencies.
	--rerun-tasks           Ignore previously cached task results.
	-S, --full-stacktrace   Print out the full (very verbose) stacktrace for all exceptions.
	-s, --stacktrace        Print out the stacktrace for all exceptions.
	--stop                  Stops the Gradle daemon if it is running.
	-u, --no-search-upward  Don't search in parent folders for a settings.gradle file.
	-v, --version           Print version info.
	-x, --exclude-task      Specify a task to be excluded from execution.

### gradlew tasks
$ gradlew tasks

:tasks

	------------------------------------------------------------
	All tasks runnable from root project
	------------------------------------------------------------
	
	Android tasks
	-------------
	androidDependencies - Displays the Android dependencies of the project.
	signingReport - Displays the signing info for each variant.
	sourceSets - Prints out all the source sets defined in this project.
	
	Build tasks
	-----------
	assemble - Assembles all variants of all applications and secondary packages.
	assembleAndroidTest - Assembles all the Test applications.
	assembleDebug - Assembles all Debug builds.
	assembleRelease - Assembles all Release builds.
	build - Assembles and tests this project.
	buildDependents - Assembles and tests this project and all projects that depend on it.
	buildNeeded - Assembles and tests this project and all projects it depends on.
	compileDebugAndroidTestSources
	compileDebugSources
	compileDebugUnitTestSources
	compileReleaseSources
	compileReleaseUnitTestSources
	extractDebugAnnotations - Extracts Android annotations for the debug variant into the archive file
	extractReleaseAnnotations - Extracts Android annotations for the release variant into the archive file
	mockableAndroidJar - Creates a version of android.jar that's suitable for unit tests.
	
	Build Setup tasks
	-----------------
	init - Initializes a new Gradle build. [incubating]
	wrapper - Generates Gradle wrapper files. [incubating]
	
	Help tasks
	----------
	components - Displays the components produced by root project 'myproject'. [incubating]
	dependencies - Displays all dependencies declared in root project 'myproject'.
	dependencyInsight - Displays the insight into a specific dependency in root project 'myproject'.
	help - Displays a help message.
	model - Displays the configuration model of root project 'myproject'. [incubating]
	projects - Displays the sub-projects of root project 'myproject'.
	properties - Displays the properties of root project 'myproject'.
	tasks - Displays the tasks runnable from root project 'myproject' (some of the displayed tasks may belong to subprojects).
	
	Install tasks
	-------------
	installDebug - Installs the Debug build.
	installDebugAndroidTest - Installs the android (on device) tests for the Debug build.
	installRelease - Installs the Release build.
	uninstallAll - Uninstall all applications.
	uninstallDebug - Uninstalls the Debug build.
	uninstallDebugAndroidTest - Uninstalls the android (on device) tests for the Debug build.
	uninstallRelease - Uninstalls the Release build.
	
	React tasks
	-----------
	bundleDebugJsAndAssets - bundle JS and assets for Debug.
	bundleReleaseJsAndAssets - bundle JS and assets for Release.
	
	Verification tasks
	------------------
	check - Runs all checks.
	clean - Deletes the build directory.
	connectedAndroidTest - Installs and runs instrumentation tests for all flavors on connected devices.
	connectedCheck - Runs all device checks on currently connected devices.
	connectedDebugAndroidTest - Installs and runs the tests for debug on connected devices.
	deviceAndroidTest - Installs and runs instrumentation tests using all Device Providers.
	deviceCheck - Runs all device checks using Device Providers and Test Servers.
	lint - Runs lint on all variants.
	lintDebug - Runs lint on the Debug build.
	lintRelease - Runs lint on the Release build.
	test - Run unit tests for all variants.
	testDebugUnitTest - Run unit tests for the debug build.
	testReleaseUnitTest - Run unit tests for the release build.
	
	Other tasks
	-----------
	assembleDefault
	copyDownloadableDepsToLibs
	jarDebugClasses
	jarReleaseClasses
	
	To see all tasks and more detail, run gradlew tasks --all
	
	To see more detail about a task, run gradlew help --task <task>


*Note: see [here](https://docs.gradle.org/current/userguide/feature_lifecycle.html "here") for description on the meaning of "incubating" in regards to gradle*