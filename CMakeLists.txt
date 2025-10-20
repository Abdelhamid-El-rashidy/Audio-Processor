cmake_minimum_required(VERSION 3.22)
project(AudioProcessor VERSION 0.0.1)

# Tell CMake to use the local JUCE folder instead of searching system-wide
add_subdirectory(JUCE)

juce_add_gui_app(AudioProcessor
        PRODUCT_NAME "Audio Processor")

target_sources(AudioProcessor PRIVATE
        Main.cpp
        MainComponent.cpp)

target_compile_definitions(AudioProcessor PRIVATE
        JUCE_WEB_BROWSER=0
        JUCE_USE_CURL=0
        JUCE_APPLICATION_NAME_STRING="$<TARGET_PROPERTY:AudioProcessor,JUCE_PRODUCT_NAME>"
        JUCE_APPLICATION_VERSION_STRING="$<TARGET_PROPERTY:AudioProcessor,JUCE_VERSION>")

target_link_libraries(AudioProcessor PRIVATE
        juce::juce_gui_extra
        juce::juce_audio_basics
        juce::juce_audio_formats
        juce::juce_audio_devices
        juce::juce_audio_utils
        PUBLIC
        juce::juce_recommended_config_flags
        juce::juce_recommended_lto_flags
        juce::juce_recommended_warning_flags)
