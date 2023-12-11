cmake_minimum_required(VERSION 3.25)

project(IJHPCASpecialIssue_VTKm NONE)

include(UseLATEX.cmake)

file(GLOB sections
  RELATIVE "${CMAKE_CURRENT_SOURCE_DIR}"
  CONFIGURE_DEPENDS
  sections/*.tex
  )

add_latex_document(IJHPCASpecialIssue_VTKm.tex
  INPUTS ${sections}
  BIBFILES IJHPCASpecialIssue_VTKm.bib
  IMAGE_DIRS figures
  )
