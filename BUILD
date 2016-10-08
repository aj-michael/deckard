#load("@io_bazel_rules_android//robolectric-extension:robolectric.bzl", "robolectric_test")
load("//rules_android/robolectric-extension:robolectric.bzl", "robolectric_test")

android_binary(
    name = "deckard",
    custom_package = "com.example",
    manifest = "src/main/java/com/example/AndroidManifest.xml",
    resource_files = glob(["src/main/java/com/example/res/**"]),
    deps = [":activity"],
)

#android_library(
#    name = "lib",
#    srcs = glob(["src/main/java/com/example/**/*.java"]),
#    #custom_package = "com.example",
#    manifest = "src/main/AndroidManifest.xml",
#    resource_files = glob(["src/main/res/**"]),
#)

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
    deps = [
        ":activity",
        "@local_robolectric_3_1_2//:jars",
    ],
)
