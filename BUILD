load("@io_bazel_rules_android//:robolectric.bzl", "robolectric_test")

android_binary(
    name = "deckard",
    custom_package = "com.example",
    manifest = "src/main/java/com/example/AndroidManifest.xml",
    resource_files = glob(["src/main/java/com/example/res/**"]),
    deps = [":activity"],
)

android_library(
    name = "activity",
    srcs = glob(["src/main/java/com/example/activity/*.java"]),
    custom_package = "com.example.activity",
    manifest = "src/main/java/com/example/activity/AndroidManifest.xml",
    resource_files = glob(["src/main/java/com/example/activity/res/**"]),
)

robolectric_test(
    name = "DeckardActivityTest",
    srcs = ["src/test/java/com/example/activity/DeckardActivityTest.java"],
    android_os_versions = [
        "6.0.0",
        "5.1.1",
        "5.0.0",
    ],
    robolectric_version = "3.1.2",
    deps = [":activity"],
)
