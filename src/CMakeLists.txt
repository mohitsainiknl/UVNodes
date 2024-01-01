
set( SOURCE
    main.cpp
)
 

qt_add_executable(${PROJECT_NAME} ${SOURCE})


target_link_libraries(${PROJECT_NAME} PRIVATE
    QtNodes
    Qt6::Core
    Qt6::Gui
    Qt6::Widgets
)

