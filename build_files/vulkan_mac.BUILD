load("@rules_cc//cc:defs.bzl", "cc_import", "cc_library")

cc_import(
    name = "vulkan_mac_private",
    shared_library = "lib/libvulkan.1.dylib",
)

cc_library(
    name = "vulkan_mac",
    hdrs = glob([
        "include/**/*.hpp",
        "include/**/*.h",
    ]),
    strip_include_prefix = "include",
    visibility = ["//visibility:public"],
    deps = [":vulkan_mac_private"],
)
