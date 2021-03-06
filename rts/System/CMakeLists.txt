
# This list was created using this *nix shell command:
# > find . -name "*.cpp" -or -name "*.c" | sort
# Then Sound/ stuff was removed, because it is now a separate static lib.
MakeGlobalVar(sources_engine_System_common
		"${CMAKE_CURRENT_SOURCE_DIR}/AIScriptHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Color.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Config/ConfigHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Config/ConfigLocater.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Config/ConfigSource.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Config/ConfigVariable.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/CRC.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/EventClient.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/EventHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/GlobalConfig.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Info.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Input/InputHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Input/Joystick.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Input/KeyInput.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Input/MouseInput.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/LoadSave/CregLoadSaveHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/LoadSave/Demo.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/LoadSave/DemoReader.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/LoadSave/DemoRecorder.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/LoadSave/LoadSaveHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/LoadSave/LuaLoadSaveHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/LogOutput.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Main.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Matrix44f.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Misc/RectangleOptimizer.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Misc/SpringTime.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Object.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/OffscreenGLContext.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Option.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Battery.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Clipboard.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/errorhandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Misc.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/SharedLib.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/ScopedFileLock.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/SDL1_keysym.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Watchdog.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/WindowManagerHelper.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Rectangle.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/SafeVector.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/SafeCStrings.c"
		"${CMAKE_CURRENT_SOURCE_DIR}/SpringApp.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/StartScriptGen.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/DumpState.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/FPUCheck.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/Logger.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/SyncChecker.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/SyncDebugger.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/SyncTracer.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/SyncedFloat3.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/backtrace.c"
		"${CMAKE_CURRENT_SOURCE_DIR}/Sync/get_executable_name.c"
		"${CMAKE_CURRENT_SOURCE_DIR}/TdfParser.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/ThreadPool.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/TimeProfiler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/TimeUtil.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/UriParser.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Util.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/type2.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/float3.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/float4.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/myMath.cpp"
	)
if    (NO_CREG)
	MakeGlobalVar(sources_engine_System_creg )
else  (NO_CREG)
	MakeGlobalVar(sources_engine_System_creg
			"${CMAKE_CURRENT_SOURCE_DIR}/creg/Serializer.cpp"
			"${CMAKE_CURRENT_SOURCE_DIR}/creg/VarTypes.cpp"
			"${CMAKE_CURRENT_SOURCE_DIR}/creg/creg.cpp"
			"${CMAKE_CURRENT_SOURCE_DIR}/creg/creg_runtime_tests.cpp"
		)
endif (NO_CREG)
MakeGlobalVar(sources_engine_System_FileSystem
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/ArchiveNameResolver.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/ArchiveLoader.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/ArchiveScanner.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/CacheDir.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/DataDirLocater.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/DataDirsAccess.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/FileFilter.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/FileHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/FileSystem.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/FileSystemAbstraction.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/FileSystemInitializer.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/GZFileHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/RapidHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/SimpleParser.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/FileSystem/VFSHandler.cpp"
	)
MakeGlobalVar(sources_engine_System_Log
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/Backend.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/DefaultFilter.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/DefaultFormatter.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/FramePrefixer.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/LogSinkHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/LogUtil.c"
	)
MakeGlobalVar(sources_engine_System_Log_sinkStream
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/StreamSink.cpp"
	)
MakeGlobalVar(sources_engine_System_Log_sinkConsole
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/ConsoleSink.cpp"
	)
MakeGlobalVar(sources_engine_System_Log_sinkFile
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/FileSink.cpp"
	)
MakeGlobalVar(sources_engine_System_Log_sinkOutputDebugString
		"${CMAKE_CURRENT_SOURCE_DIR}/Log/OutputDebugStringSink.cpp"
	)
Set(sources_engine_System_Platform_Linux
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Linux/CrashHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Linux/SoLib.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Linux/MessageBox.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Linux/WindowManagerHelper.cpp"
	)
Set(sources_engine_System_Platform_Mac
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Linux/SoLib.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Mac/MessageBox.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Mac/CrashHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Mac/WindowManagerHelper.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Linux/ThreadSupport.cpp"
	)
Set(sources_engine_System_Platform_Windows
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Win/CrashHandler.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Win/DllLib.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Win/MessageBox.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Win/seh.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Win/WinVersion.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Win/WindowManagerHelper.cpp"
	)

Set(sources_engine_System_Threading_Mac
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Mac/Signal.cpp"
	)
Set(sources_engine_System_Threading_Linux
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Linux/Futex.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Linux/ThreadSupport.cpp"
	)
Set(sources_engine_System_Threading_Windows
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Win/CriticalSection.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Win/Future.cpp"
	)


if(CMAKE_VERSION VERSION_GREATER 3.1.2)
	target_sources(platform_sources
		PRIVATE
			${sources_engine_System_Platform_Windows}
			${sources_engine_System_Platform_Linux}
			${sources_engine_System_Platform_Mac}
			${sources_engine_System_Threading_Windows}
			${sources_engine_System_Threading_Linux}
			${sources_engine_System_Threading_Mac}
		)
endif()

Set(sources_engine_System_Threading
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/CpuID.cpp"
		"${CMAKE_CURRENT_SOURCE_DIR}/Platform/Threading.cpp"
	)

Set(sources_engine_System
		${sources_engine_System_common}
		${sources_engine_System_creg}
		${sources_engine_System_FileSystem}
		${sources_engine_System_Log}
		${sources_engine_System_Log_sinkConsole}
		${sources_engine_System_Log_sinkFile}
	)


### only use the target platform related directory
IF     (APPLE)
	MakeGlobalVar(sources_engine_System_Threading ${sources_engine_System_Threading} ${sources_engine_System_Threading_Mac})
	MakeGlobalVar(sources_engine_System
			${sources_engine_System}
			${sources_engine_System_Threading}
		)
ELSEIF (UNIX)
	MakeGlobalVar(sources_engine_System_Threading ${sources_engine_System_Threading} ${sources_engine_System_Threading_Linux})
	MakeGlobalVar(sources_engine_System
			${sources_engine_System}
			${sources_engine_System_Platform_Linux}
			${sources_engine_System_Threading}
		)

ELSEIF (WIN32)
	MakeGlobalVar(sources_engine_System_Threading ${sources_engine_System_Threading} ${sources_engine_System_Threading_Windows})
	MakeGlobalVar(sources_engine_System
			${sources_engine_System}
			${sources_engine_System_Log_sinkOutputDebugString}
			${sources_engine_System_Platform_Windows}
			${sources_engine_System_Threading}
		)
ELSE()
	MakeGlobalVar(sources_engine_System
			${sources_engine_System}
			${sources_engine_System_Threading}
		)
ENDIF  ()


Add_Subdirectory(FileSystem)
Add_Subdirectory(Net)
