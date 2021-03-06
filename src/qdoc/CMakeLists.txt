# Generated from qdoc.pro.

# special case begin
if(CMAKE_VERSION VERSION_LESS "3.19" AND MSVC AND CMAKE_GENERATOR STREQUAL "Ninja Multi-Config")
    message(WARNING "qdoc will not be built in this configuration.")
    return()
endif()
# special case end

#####################################################################
## qdoc Tool:
#####################################################################

qt_get_tool_target_name(target_name qdoc)
qt_internal_add_tool(${target_name}
    TARGET_DESCRIPTION "Qt Documentation Compiler"
    TOOLS_TARGET Tools # special case
    SOURCES
        access.h
        aggregate.cpp aggregate.h
        atom.cpp atom.h
        clangcodeparser.cpp clangcodeparser.h
        classnode.cpp classnode.h
        codechunk.cpp codechunk.h
        codemarker.cpp codemarker.h
        codeparser.cpp codeparser.h
        collectionnode.cpp collectionnode.h
        config.cpp config.h
        cppcodemarker.cpp cppcodemarker.h
        cppcodeparser.cpp cppcodeparser.h
        doc.cpp doc.h
        docbookgenerator.cpp docbookgenerator.h
        docparser.cpp docparser.h
        docprivate.cpp docprivate.h
        docutilities.h
        editdistance.cpp editdistance.h
        enumitem.h
        enumnode.cpp enumnode.h
        examplenode.h
        externalpagenode.cpp externalpagenode.h
        functionnode.cpp functionnode.h
        generator.cpp generator.h
        headernode.cpp headernode.h
        helpprojectwriter.cpp helpprojectwriter.h
        htmlgenerator.cpp htmlgenerator.h
        importrec.h
        jscodemarker.cpp jscodemarker.h
        location.cpp location.h
        macro.h
        main.cpp
        manifestwriter.cpp manifestwriter.h
        namespacenode.cpp namespacenode.h
        node.cpp node.h
        openedlist.cpp openedlist.h
        pagenode.cpp pagenode.h
        parameters.cpp parameters.h
        propertynode.cpp propertynode.h
        proxynode.cpp proxynode.h
        puredocparser.cpp puredocparser.h
        qdoccommandlineparser.cpp qdoccommandlineparser.h
        qdocdatabase.cpp qdocdatabase.h
        qdocindexfiles.cpp qdocindexfiles.h
        qmlcodemarker.cpp qmlcodemarker.h
        qmlcodeparser.cpp qmlcodeparser.h
        qmlmarkupvisitor.cpp qmlmarkupvisitor.h
        qmlpropertynode.cpp qmlpropertynode.h
        qmltypenode.cpp qmltypenode.h
        qmlvisitor.cpp qmlvisitor.h
        quoter.cpp quoter.h
        relatedclass.cpp relatedclass.h
        sections.cpp sections.h
        sharedcommentnode.cpp sharedcommentnode.h
        singleton.h
        tagfilewriter.cpp tagfilewriter.h
        text.cpp text.h
        tokenizer.cpp tokenizer.h
        topic.h
        tree.cpp tree.h
        typedefnode.cpp typedefnode.h
        usingclause.cpp usingclause.h
        utilities.cpp utilities.h
        variablenode.cpp variablenode.h
        webxmlgenerator.cpp webxmlgenerator.h
        xmlgenerator.cpp xmlgenerator.h
    LIBRARIES # special case
        WrapLibClang::WrapLibClang # special case
    DEFINES
        #(CLANG_RESOURCE_DIR=\"/clang//include\") # special case remove
        CLANG_RESOURCE_DIR=${QT_LIBCLANG_RESOURCE_DIR} # special case
        QDOC2_COMPAT
    INCLUDE_DIRECTORIES
        ${QT_SOURCE_TREE}/src/tools/qdoc
        ${QT_SOURCE_TREE}/src/tools/qdoc/qmlparser
)

#### Keys ignored in scope 1:.:.:qdoc.pro:<TRUE>:
# CMAKE_BIN_DIR = "$$cmakeRelativePath($$[QT_HOST_BINS], $$[QT_INSTALL_PREFIX])"
# CMAKE_INSTALL_LIBS_DIR = "$$cmakeTargetPath($$[QT_INSTALL_LIBS])"
# CMAKE_LIB_DIR = "$$cmakeRelativePath($$[QT_INSTALL_LIBS], $$[QT_INSTALL_PREFIX])"
# CMAKE_PACKAGE_VERSION = "$$MODULE_VERSION"
# INSTALLS = "cmake_qdoc_tools_files"
# QMAKE_SUBSTITUTES = "cmake_qdoc_config_file" "cmake_qdoc_config_version_file"
# QMAKE_TARGET_DESCRIPTION = "Qt Documentation Compiler"
# TR_EXCLUDE = "$$PWD/*"
# _OPTION = "host_build"
# cmake_qdoc_config_file.input = "$$PWD/Qt5DocToolsConfig.cmake.in"
# cmake_qdoc_config_file.output = "$$MODULE_BASE_OUTDIR/lib/cmake/Qt5DocTools/Qt5DocToolsConfig.cmake"
# cmake_qdoc_config_version_file.input = "$$[QT_HOST_DATA/src]/mkspecs/features/data/cmake/Qt5ConfigVersion.cmake.in"
# cmake_qdoc_config_version_file.output = "$$MODULE_BASE_OUTDIR/lib/cmake/Qt5DocTools/Qt5DocToolsConfigVersion.cmake"
# cmake_qdoc_tools_files.CONFIG = "no_check_exist"
# cmake_qdoc_tools_files.files = "$$cmake_qdoc_config_file.output" "$$cmake_qdoc_config_version_file.output"
# cmake_qdoc_tools_files.path = "$$[QT_INSTALL_LIBS]/cmake/Qt5DocTools"

## Scopes:
#####################################################################

#### Keys ignored in scope 2:.:.:qdoc.pro:NOT force_bootstrap:
# _REQUIREMENTS = "qtConfig(xmlstreamwriter)"

qt_internal_extend_target(${target_name} CONDITION TARGET Qt::QmlDevToolsPrivate
    PUBLIC_LIBRARIES
        Qt::QmlDevToolsPrivate
)

qt_internal_extend_target(${target_name} CONDITION NOT TARGET Qt::QmlDevToolsPrivate
    DEFINES
        QT_NO_DECLARATIVE
)

#### Keys ignored in scope 6:.:.:qdoc.pro:NOT QMAKE_DEFAULT_LIBDIRS___contains____ss_CLANG_LIBDIR AND NOT disable_external_rpath:
# QMAKE_RPATHDIR = "$$CLANG_LIBDIR"

qt_internal_extend_target(${target_name} CONDITION win32-icc_x_ OR win32-msvc_x_
    LINK_OPTIONS
        "/STACK:4194304"
)

#### Keys ignored in scope 8:.:.:qdoc.pro:CMAKE_INSTALL_LIBS_DIR___contains___^(/usr?/lib(64)?._x_):
# CMAKE_USR_MOVE_WORKAROUND = "$$CMAKE_INSTALL_LIBS_DIR"

#### Keys ignored in scope 9:.:.:qdoc.pro:NOT CMAKE_LIB_DIR___contains___^\\.\\./._x_:
# CMAKE_RELATIVE_INSTALL_DIR = "$${CMAKE_RELATIVE_INSTALL_LIBS_DIR}../../"
# CMAKE_RELATIVE_INSTALL_LIBS_DIR = "$$cmakeRelativePath($$[QT_INSTALL_PREFIX], $$[QT_INSTALL_LIBS])"

#### Keys ignored in scope 10:.:.:qdoc.pro:else:
# CMAKE_LIB_DIR_IS_ABSOLUTE = "True"

#### Keys ignored in scope 11:.:.:qdoc.pro:CMAKE_BIN_DIR___contains___^\\.\\./._x_:
# CMAKE_BIN_DIR = "$$[QT_HOST_BINS]/"
# CMAKE_BIN_DIR_IS_ABSOLUTE = "True"

#### Keys ignored in scope 12:.:.:qdoc.pro:QMAKE_HOST.os___equals___Windows:
# CMAKE_BIN_SUFFIX = ".exe"
qt_internal_add_docs(${target_name}
    doc/config/qdoc.qdocconf
)

