# Find src
file(GLOB_RECURSE CRAP_SOURCES    *.cpp)
file(GLOB_RECURSE CRAP_HEADERS    *.h)
#file(GLOB_RECURSE CRAP_FORMS      *.ui)

# QT wrap
#QT5_WRAP_UI(CRAP_FORMS_HEADERS ${CRAP_FORMS})
#QT5_ADD_RESOURCES(CRAP_RESOURCES_RCC ${CRAP_RESOURCES})
  
# Make app
add_executable(sample
  ${CRAP_SOURCES}
  ${CRAP_FORMS_HEADERS}
)

## Use the Widgets module from Qt 5.
target_link_libraries(sample Qt5::Core)


