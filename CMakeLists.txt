cmake_minimum_required(VERSION 3.20)

set(PDFLATEX_COMPILER xelatex) # Use XeLaTeX for compilation
set(FONT_DIR fonts)
project(CV-RESUME NONE)

  include(UseLATEX.cmake)

  add_latex_document(cv.tex TARGET_NAME cv
          INPUTS cv/education.tex
                 cv/skills.tex
                 cv/experience.tex
                 cv/extracurricular.tex
                 cv/honors.tex
                 cv/presentation.tex
                 cv/writing.tex
                 cv/committees.tex
                 awesome-cv.cls

                 ${FONT_DIR}/FontAwesome.ttf
                 ${FONT_DIR}/Roboto-Regular.ttf
                 ${FONT_DIR}/Roboto-Italic.ttf
                 ${FONT_DIR}/Roboto-Light.ttf
                 ${FONT_DIR}/Roboto-LightItalic.ttf
                 ${FONT_DIR}/Roboto-Thin.ttf
                 ${FONT_DIR}/Roboto-ThinItalic.ttf
                 ${FONT_DIR}/Roboto-Bold.ttf
                 ${FONT_DIR}/Roboto-BoldItalic.ttf
                 ${FONT_DIR}/Roboto-Medium.ttf
                 ${FONT_DIR}/Roboto-MediumItalic.ttf
          # BIBFILES bibliography.bib
          USE_BIBLATEX
          IMAGE_DIRS assets/images
          #  USE_INDEX
          EXCLUDE_FROM_ALL
  )

  add_latex_document(resume.tex TARGET_NAME resume
         INPUTS resume/education.tex
                resume/experience.tex
                resume/extracurricular.tex
                resume/summary.tex
                resume/honors.tex
                resume/presentation.tex
                resume/writing.tex
                resume/committees.tex
                awesome-cv.cls

                ${FONT_DIR}/FontAwesome.ttf
                ${FONT_DIR}/Roboto-Regular.ttf
                ${FONT_DIR}/Roboto-Italic.ttf
                ${FONT_DIR}/Roboto-Light.ttf
                ${FONT_DIR}/Roboto-LightItalic.ttf
                ${FONT_DIR}/Roboto-Thin.ttf
                ${FONT_DIR}/Roboto-ThinItalic.ttf
                ${FONT_DIR}/Roboto-Bold.ttf
                ${FONT_DIR}/Roboto-BoldItalic.ttf
                ${FONT_DIR}/Roboto-Medium.ttf
                ${FONT_DIR}/Roboto-MediumItalic.ttf
        # BIBFILES bibliography.bib
        USE_BIBLATEX
        IMAGE_DIRS assets/images
        #  USE_INDEX
        EXCLUDE_FROM_ALL
)

  add_latex_document(coverletter.tex TARGET_NAME coverletter
        INPUTS  awesome-cv.cls

        ${FONT_DIR}/FontAwesome.ttf
        ${FONT_DIR}/Roboto-Regular.ttf
        ${FONT_DIR}/Roboto-Italic.ttf
        ${FONT_DIR}/Roboto-Light.ttf
        ${FONT_DIR}/Roboto-LightItalic.ttf
        ${FONT_DIR}/Roboto-Thin.ttf
        ${FONT_DIR}/Roboto-ThinItalic.ttf
        ${FONT_DIR}/Roboto-Bold.ttf
        ${FONT_DIR}/Roboto-BoldItalic.ttf
        ${FONT_DIR}/Roboto-Medium.ttf
        ${FONT_DIR}/Roboto-MediumItalic.ttf
        # BIBFILES bibliography.bib
        USE_BIBLATEX
        IMAGE_DIRS assets/images
        #  USE_INDEX
        EXCLUDE_FROM_ALL
)


