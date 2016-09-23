#load("@io_bazel_rules_android//robolectric-extension:robolectric.bzl", "robolectric_test")
load("//rules_android/robolectric-extension:robolectric.bzl", "robolectric_test")

android_binary(
    name = "deckard",
    custom_package = "com.example",
    manifest = "src/main/AndroidManifest.xml",
    resource_files = glob(["src/main/res/**"]),
    deps = ["//src/main/java/com/example:lib"],
)

robolectric_test(
    name = "DeckardActivityTest",
    srcs = ["src/test/java/com/example/activity/DeckardActivityTest.java"],
    deps = ["//src/main/java/com/example:lib"],
)
