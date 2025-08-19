project(tclapExamples LANGUAGES CXX)

# prepare a set of samples dependent on the above library
set(SAMPLES_LIST
    test10.cpp
    test11.cpp
    test12.cpp
    test13.cpp
    test14.cpp
    test15.cpp
    test16.cpp
    test18.cpp
    test19.cpp
    test1.cpp
    test20.cpp
    test21.cpp
    test22.cpp
    test23.cpp
    test24.cpp
    test25.cpp
    test26.cpp
    test27.cpp
    test28.cpp
    test29.cpp
    test2.cpp
    test30.cpp
    test3.cpp
    test4.cpp
    test5.cpp
    test6.cpp
    test7.cpp
    test8.cpp
    test9.cpp
    # test-hard-1.cpp #this does not have a main()
    test-hard-2.cpp
    )

foreach(s ${SAMPLES_LIST})
	get_filename_component(sn "${s}" NAME_WE)
	cs_add_executable(tclapExamples_${sn})
	cs_target_sources(tclapExamples_${sn} PRIVATE ${s})
	cs_target_link_libraries(tclapExamples_${sn} PRIVATE tclap::tclap)
	cs_install_target(tclapExamples_${sn} tclapExamples_${sn})
	cs_finalize_target(tclapExamples_${sn})
endforeach()
