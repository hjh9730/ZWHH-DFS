#set src directory list
aux_source_directory(. SRC_LIST)

#build link
add_library(source-objects OBJECT ${SRC_LIST})

#transport link
set(source
    $<TARGET_OBJECT:source-objects>
    PARENT_SCOPE)
