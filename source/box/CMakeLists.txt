set(TestName "TestBox")

add_executable(${TestName}
        test_box.cpp)

set("CompileOptionsNotWithCatch2"
        -Wno-multiple-inheritance)

target_compile_options(${TestName}
        PRIVATE
        ${CompileOptionsGccExhaustive}
        ${CompileOptionsNotWithCatch2})

target_link_libraries(${TestName}
        PRIVATE
        Catch2::Catch2WithMain)
