# Command Reference

28th August 2016

*warning: this stuff is constantly changing, and may become out of date soon.*

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

---

### adb

$ adb --help


	Android Debug Bridge version 1.0.36
	Revision af05c7354fe1-android
	
	 -a                            - directs adb to listen on all interfaces for a connection
	 -d                            - directs command to the only connected USB device
	                                 returns an error if more than one USB device is present.
	 -e                            - directs command to the only running emulator.
	                                 returns an error if more than one emulator is running.
	 -s <specific device>          - directs command to the device or emulator with the given
	                                 serial number or qualifier. Overrides ANDROID_SERIAL
	                                 environment variable.
	 -p <product name or path>     - simple product name like 'sooner', or
	                                 a relative/absolute path to a product
	                                 out directory like 'out/target/product/sooner'.
	                                 If -p is not specified, the ANDROID_PRODUCT_OUT
	                                 environment variable is used, which must
	                                 be an absolute path.
	 -H                            - Name of adb server host (default: localhost)
	 -P                            - Port of adb server (default: 5037)
	 devices [-l]                  - list all connected devices
	                                 ('-l' will also list device qualifiers)
	 connect <host>[:<port>]       - connect to a device via TCP/IP
	                                 Port 5555 is used by default if no port number is specified.
	 disconnect [<host>[:<port>]]  - disconnect from a TCP/IP device.
	                                 Port 5555 is used by default if no port number is specified.
	                                 Using this command with no additional arguments
	                                 will disconnect from all connected TCP/IP devices.
	
	device commands:
	  adb push <local>... <remote>
	                               - copy files/dirs to device
	  adb pull [-a] <remote>... <local>
	                               - copy files/dirs from device
	                                 (-a preserves file timestamp and mode)
	  adb sync [ <directory> ]     - copy host->device only if changed
	                                 (-l means list but don't copy)
	  adb shell [-e escape] [-n] [-Tt] [-x] [command]
	                               - run remote shell command (interactive shell if no command given)
	                                 (-e: choose escape character, or "none"; default '~')
	                                 (-n: don't read from stdin)
	                                 (-T: disable PTY allocation)
	                                 (-t: force PTY allocation)
	                                 (-x: disable remote exit codes and stdout/stderr separation)
	  adb emu <command>            - run emulator console command
	  adb logcat [ <filter-spec> ] - View device log
	  adb forward --list           - list all forward socket connections.
	                                 the format is a list of lines with the following format:
	                                    <serial> " " <local> " " <remote> "\n"
	  adb forward <local> <remote> - forward socket connections
	                                 forward specs are one of:
	                                   tcp:<port>
	                                   localabstract:<unix domain socket name>
	                                   localreserved:<unix domain socket name>
	                                   localfilesystem:<unix domain socket name>
	                                   dev:<character device name>
	                                   jdwp:<process pid> (remote only)
	  adb forward --no-rebind <local> <remote>
	                               - same as 'adb forward <local> <remote>' but fails
	                                 if <local> is already forwarded
	  adb forward --remove <local> - remove a specific forward socket connection
	  adb forward --remove-all     - remove all forward socket connections
	  adb reverse --list           - list all reverse socket connections from device
	  adb reverse <remote> <local> - reverse socket connections
	                                 reverse specs are one of:
	                                   tcp:<port>
	                                   localabstract:<unix domain socket name>
	                                   localreserved:<unix domain socket name>
	                                   localfilesystem:<unix domain socket name>
	  adb reverse --no-rebind <remote> <local>
	                               - same as 'adb reverse <remote> <local>' but fails
	                                 if <remote> is already reversed.
	  adb reverse --remove <remote>
	                               - remove a specific reversed socket connection
	  adb reverse --remove-all     - remove all reversed socket connections from device
	  adb jdwp                     - list PIDs of processes hosting a JDWP transport
	  adb install [-lrtsdg] <file>
	                               - push this package file to the device and install it
	                                 (-l: forward lock application)
	                                 (-r: replace existing application)
	                                 (-t: allow test packages)
	                                 (-s: install application on sdcard)
	                                 (-d: allow version code downgrade (debuggable packages only))
	                                 (-g: grant all runtime permissions)
	  adb install-multiple [-lrtsdpg] <file...>
	                               - push this package file to the device and install it
	                                 (-l: forward lock application)
	                                 (-r: replace existing application)
	                                 (-t: allow test packages)
	                                 (-s: install application on sdcard)
	                                 (-d: allow version code downgrade (debuggable packages only))
	                                 (-p: partial application install)
	                                 (-g: grant all runtime permissions)
	  adb uninstall [-k] <package> - remove this app package from the device
	                                 ('-k' means keep the data and cache directories)
	  adb bugreport [<zip_file>]   - return all information from the device
	                                 that should be included in a bug report.
	
	  adb backup [-f <file>] [-apk|-noapk] [-obb|-noobb] [-shared|-noshared] [-all] [-system|-nosystem] [<packages...>]
	                               - write an archive of the device's data to <file>.
	                                 If no -f option is supplied then the data is written
	                                 to "backup.ab" in the current directory.
	                                 (-apk|-noapk enable/disable backup of the .apks themselves
	                                    in the archive; the default is noapk.)
	                                 (-obb|-noobb enable/disable backup of any installed apk expansion
	                                    (aka .obb) files associated with each application; the default
	                                    is noobb.)
	                                 (-shared|-noshared enable/disable backup of the device's
	                                    shared storage / SD card contents; the default is noshared.)
	                                 (-all means to back up all installed applications)
	                                 (-system|-nosystem toggles whether -all automatically includes
	                                    system applications; the default is to include system apps)
	                                 (<packages...> is the list of applications to be backed up.  If
	                                    the -all or -shared flags are passed, then the package
	                                    list is optional.  Applications explicitly given on the
	                                    command line will be included even if -nosystem would
	                                    ordinarily cause them to be omitted.)
	
	  adb restore <file>           - restore device contents from the <file> backup archive
	
	  adb disable-verity           - disable dm-verity checking on USERDEBUG builds
	  adb enable-verity            - re-enable dm-verity checking on USERDEBUG builds
	  adb keygen <file>            - generate adb public/private key. The private key is stored in <file>,
	                                 and the public key is stored in <file>.pub. Any existing files
	                                 are overwritten.
	  adb help                     - show this help message
	  adb version                  - show version num
	
	scripting:
	  adb wait-for[-<transport>]-<state>
	                               - wait for device to be in the given state:
	                                 device, recovery, sideload, or bootloader
	                                 Transport is: usb, local or any [default=any]
	  adb start-server             - ensure that there is a server running
	  adb kill-server              - kill the server if it is running
	  adb get-state                - prints: offline | bootloader | device
	  adb get-serialno             - prints: <serial-number>
	  adb get-devpath              - prints: <device-path>
	  adb remount                  - remounts the /system, /vendor (if present) and /oem (if present) partitions on the device read-write
	  adb reboot [bootloader|recovery]
	                               - reboots the device, optionally into the bootloader or recovery program.
	  adb reboot sideload          - reboots the device into the sideload mode in recovery program (adb root required).
	  adb reboot sideload-auto-reboot
	                               - reboots into the sideload mode, then reboots automatically after the sideload regardless of the result.
	  adb sideload <file>          - sideloads the given package
	  adb root                     - restarts the adbd daemon with root permissions
	  adb unroot                   - restarts the adbd daemon without root permissions
	  adb usb                      - restarts the adbd daemon listening on USB
	  adb tcpip <port>             - restarts the adbd daemon listening on TCP on the specified port
	
	networking:
	  adb ppp <tty> [parameters]   - Run PPP over USB.
	 Note: you should not automatically start a PPP connection.
	 <tty> refers to the tty for PPP stream. Eg. dev:/dev/omap_csmi_tty1
	 [parameters] - Eg. defaultroute debug dump local notty usepeerdns
	
	adb sync notes: adb sync [ <directory> ]
	  <localdir> can be interpreted in several ways:
	
	  - If <directory> is not specified, /system, /vendor (if present), /oem (if present) and /data partitions will be updated.
	
	  - If it is "system", "vendor", "oem" or "data", only the corresponding partition
	    is updated.
	
	internal debugging:
	  adb reconnect                  Kick current connection from host side and make it reconnect.
	  adb reconnect device           Kick current connection from device side and make it reconnect.
	environment variables:
	  ADB_TRACE                    - Print debug information. A comma separated list of the following values
	                                 1 or all, adb, sockets, packets, rwx, usb, sync, sysdeps, transport, jdwp
	  ANDROID_SERIAL               - The serial number to connect to. -s takes priority over this if given.
	  ANDROID_LOG_TAGS             - When used with the logcat option, only these debug tags are printed.

### android

$ android --help

	       Usage:
	       android [global options] action [action options]
	       Global options:
	  -s --silent     : Silent mode, shows errors only.
	  -v --verbose    : Verbose mode, shows errors, warnings and all messages.
	     --clear-cache: Clear the SDK Manager repository manifest cache.
	  -h --help       : Help on a specific command.
	
	                                                                    Valid
	                                                                    actions
	                                                                    are
	                                                                    composed
	                                                                    of a verb
	                                                                    and an
	                                                                    optional
	                                                                    direct
	                                                                    object:
	-    sdk              : Displays the SDK Manager window.
	-    avd              : Displays the AVD Manager window.
	-   list              : Lists existing targets or virtual devices.
	-   list avd          : Lists existing Android Virtual Devices.
	-   list target       : Lists existing targets.
	-   list device       : Lists existing devices.
	-   list sdk          : Lists remote SDK repository.
	- create avd          : Creates a new Android Virtual Device.
	-   move avd          : Moves or renames an Android Virtual Device.
	- delete avd          : Deletes an Android Virtual Device.
	- update avd          : Updates an Android Virtual Device to match the folders
	                        of a new SDK.
	- create project      : Creates a new Android project.
	- update project      : Updates an Android project (must already have an
	                        AndroidManifest.xml).
	- create test-project : Creates a new Android project for a test package.
	- update test-project : Updates the Android project for a test package (must
	                        already have an AndroidManifest.xml).
	- create lib-project  : Creates a new Android library project.
	- update lib-project  : Updates an Android library project (must already have
	                        an AndroidManifest.xml).
	- create uitest-project: Creates a new UI test project.
	- update adb          : Updates adb to support the USB devices declared in the
	                        SDK add-ons.
	- update sdk          : Updates the SDK by suggesting new platforms to install
	                        if available.

---

### keytool

$ keytool --help

Key and Certificate Management Tool

	Commands:
	
	 -certreq            Generates a certificate request
	 -changealias        Changes an entry's alias
	 -delete             Deletes an entry
	 -exportcert         Exports certificate
	 -genkeypair         Generates a key pair
	 -genseckey          Generates a secret key
	 -gencert            Generates certificate from a certificate request
	 -importcert         Imports a certificate or a certificate chain
	 -importpass         Imports a password
	 -importkeystore     Imports one or all entries from another keystore
	 -keypasswd          Changes the key password of an entry
	 -list               Lists entries in a keystore
	 -printcert          Prints the content of a certificate
	 -printcertreq       Prints the content of a certificate request
	 -printcrl           Prints the content of a CRL file
	 -storepasswd        Changes the store password of a keystore
	
	Use "keytool -command_name -help" for usage of command_name