PROJECT(ParaViewTutorial NONE)

CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

INCLUDE(UseLATEX.cmake)

SET(PARAVIEW_VERSION "4.0")

SET(SHORT_TITLE "The ParaView Tutorial")
SET(LONG_TITLE "${SHORT_TITLE} \\\\ {\\small Version ${PARAVIEW_VERSION}}")

OPTION(SAVE_TREES "When on, tries to squeeze more on each page to reduce the number of pages needed to print the document." OFF)

IF (SAVE_TREES)
  SET(GLOBAL_OPTIONS "10pt,twocolumn,openany")
  SET(SAVE_TREES_FLAG true)
ELSE (SAVE_TREES)
  SET(GLOBAL_OPTIONS "12pt")
  SET(SAVE_TREES_FLAG false)
ENDIF (SAVE_TREES)

SET(CHAPTER_FILES
  Introduction.tex
  BasicUsage.tex
  VisualizingLargeModels.tex
  BatchPythonScripting.tex
  FurtherReading.tex
  )

ADD_LATEX_DOCUMENT(ParaViewTutorial.tex
  INPUTS ${CHAPTER_FILES}
  CONFIGURE ParaViewTutorial.tex
  IMAGE_DIRS images images/icons
  USE_INDEX
  )
