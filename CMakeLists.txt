PROJECT(ParaViewTutorial NONE)

CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

INCLUDE(UseLATEX.cmake)

SET(SHORT_TITLE "Large Scale Visualization with ParaView")
SET(LONG_TITLE "${SHORT_TITLE} \\\\ Supercomputing 2008 Tutorial")

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
