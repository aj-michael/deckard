# Setup for the android_library() and android_binary() rules.
android_sdk_repository(
    name = "androidsdk",
    # Replace with the Android SDK API level
    api_level = 24,
    # Replace with the version in sdk/build-tools/
    build_tools_version = "24.0.1",
    # Replace with path to Android SDK on your system
    path = "/usr/local/google/home/vnayar/Android/Sdk",
)

# Setup for the Bazel extension created robolectric_test() rule.
git_repository(
    name = "io_bazel_rules_android",
    commit = "af05a9d563124a83a9a738eacf82461902230e08",
    remote = "https://github.com/vnayar/rules_android.git",
)

load("@io_bazel_rules_android//:robolectric-workspace.bzl", "robolectric_jars")

robolectric_jars()
