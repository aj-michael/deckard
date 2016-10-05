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

# For local development with Robolectric.
new_local_repository(
    name = "local_robolectric_3_1_2",
    build_file_content = """
java_import(
  name = "jars",
  jars = [
    "//:robolectric/build/libs/robolectric-3.1.2.jar",
    "//:robolectric-annotations/build/libs/robolectric-annotations-3.1.2.jar",
    "//:robolectric-processor/build/libs/robolectric-processor-3.1.2.jar",
    "//:robolectric-utils/build/libs/robolectric-utils-3.1.2.jar",
    "//:robolectric-resources/build/libs/robolectric-resources-3.1.2.jar",
    "//:build/libs/robolectric-3.1.2.jar",
  ],
  visibility = ["//visibility:public"],
)
""",
    path = "/usr/local/google/home/vnayar/projects/robolectric",
)
