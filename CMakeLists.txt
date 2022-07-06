check_include_file_cxx(stdint.h HAVE_STDINT_H)
if(HAVE_STDINT_H)
    add_definitions(-DHAVE_STDINT_H)
endif()

build_lib(
    LIBNAME ns3-ai
    SOURCE_FILES model/memory-pool.cc
    HEADER_FILES model/memory-pool.h
                 model/ns3-ai-dl.h
                 model/ns3-ai-rl.h
                 model/train-var.h
    LIBRARIES_TO_LINK ${libcore}
)
    
