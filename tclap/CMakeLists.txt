project(tclap LANGUAGES CXX)

# prepare standard library
cs_add_library(tclap INTERFACE)
cs_add_library(tclap::tclap ALIAS tclap)

cs_target_sources(tclap
	PRIVATE_INSTALL
		ArgException.h
		Arg.h
		ArgTraits.h
		CMakeLists.txt
		CmdLine.h
		CmdLineInterface.h
		CmdLineOutput.h
		Constraint.h
		DocBookOutput.h
		HelpVisitor.h
		IgnoreRestVisitor.h
		MultiArg.h
		MultiSwitchArg.h
		OptionalUnlabeledTracker.h
		sstream.h
		StandardTraits.h
		StdOutput.h
		SwitchArg.h
		UnlabeledMultiArg.h
		UnlabeledValueArg.h
		ValueArg.h
		ValuesConstraint.h
		VersionVisitor.h
		Visitor.h
		XorHandler.h
		ZshCompletionOutput.h
	PRIVATE
)

cs_target_link_libraries(tclap
	INTERFACE
		tclapSol::tclapSol_csCMakeBaseInclude
)

cs_install_target(tclap tclap DEFAULT)

cs_finalize_target(tclap)
