# Command Reference

### react-native

$react-native --help

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
$gradlew.bat --help

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