INCLUDE_DIRECTORIES(${CMAKE_BINARY_DIR}/fem/src)
file(COPY ELMERSOLVER_STARTINFO DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/")
file(COPY box/mesh.boundary box/mesh.header box/mesh.nodes box/mesh.elements box/mesh.names DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/box")
file(COPY sif/box.sif DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/sif")
ADD_ELMER_TEST(mgdyn_mfd)
ADD_ELMER_LABEL(mgdyn_mfd 3D)
ADD_ELMER_LABEL(mgdyn_mfd mgdyn)
