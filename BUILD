#load("@io_bazel_rules_android//robolectric-extension:robolectric.bzl", "robolectric_test")
load("//rules_android/robolectric-extension:robolectric.bzl", "robolectric_test")

android_binary(
    name = "deckard",
    custom_package = "com.example",
    manifest = "src/main/AndroidManifest.xml",
    resource_files = glob(["src/main/res/**"]),
    deps = [":lib"],
)

android_library(
    name = "lib",
    srcs = glob(["src/main/java/com/example/**/*.java"]),
    custom_package = "com.example",
    manifest = "src/main/AndroidManifest.xml",
    resource_files = glob(["src/main/res/**"]),
)

robolectric_test(
    name = "DeckardActivityTest",
    srcs = ["src/test/java/com/example/activity/DeckardActivityTest.java"],
    deps = [
        ":lib",
        "@local_robolectric_3_1_2//:jars",
    ],
)
