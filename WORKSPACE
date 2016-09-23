# TODO(vnayar): Many of these rules may need to be migrated into the Android Robolectric Skylark extension.

android_sdk_repository(
    name = "androidsdk",
    # Replace with the Android SDK API level
    api_level = 24,
    # Replace with the version in sdk/build-tools/
    build_tools_version = "24.0.1",
    # Replace with path to Android SDK on your system
    path = "/usr/local/google/home/vnayar/Android/Sdk",
)

git_repository(
    name = "io_bazel_rules_android",
    commit = "4477aabc2d99554d17be2833de2a272472b48f76",
    remote = "https://github.com/vnayar/rules_android.git",
)

#load("@io_bazel_rules_android//robolectric-extension:robolectric-workspace.bzl", "robolectric_jars")
load("//rules_android/robolectric-extension:robolectric-workspace.bzl", "robolectric_jars")

robolectric_jars()
