add_llvm_library(MLIRLLVMIR
  IR/LLVMDialect.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/LLVMIR
  )
add_dependencies(MLIRLLVMIR MLIRLLVMOpsIncGen MLIRLLVMConversionsIncGen LLVMAsmParser LLVMCore LLVMSupport)
target_link_libraries(MLIRLLVMIR LLVMAsmParser LLVMCore LLVMSupport)

add_llvm_library(MLIRNVVMIR
  IR/NVVMDialect.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/LLVMIR
  )
add_dependencies(MLIRNVVMIR MLIRNVVMOpsIncGen MLIRNVVMConversionsIncGen LLVMAsmParser LLVMCore LLVMSupport)
target_link_libraries(MLIRNVVMIR LLVMAsmParser LLVMCore LLVMSupport)
