PROJECT(ParaViewTutorial NONE)

CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

INCLUDE(UseLATEX.cmake)

SET(PARAVIEW_VERSION "3.6")

SET(SHORT_TITLE "The ParaView Tutorial")
SET(LONG_TITLE "${SHORT_TITLE} \\\\ {\\small Version ${PARAVIEW_VERSION}}")

SET(CHAPTER_FILES
  Introduction.tex
  BasicUsage.tex
  VisualizingLargeModels.tex
  FurtherReading.tex
  )

ADD_LATEX_DOCUMENT(ParaViewTutorial.tex
  INPUTS ${CHAPTER_FILES}
  CONFIGURE ParaViewTutorial.tex
  IMAGE_DIRS images images/icons
  USE_INDEX
  )
