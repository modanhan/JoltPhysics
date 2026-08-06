load("@rules_cc//cc:defs.bzl", "cc_import", "cc_library")

cc_import(
    name = "vulkan_linux_private",
    hdrs = glob([
        "include/vulkan/**/*.hpp",
        "include/vulkan/**/*.h",
    ]),
    shared_library = "lib/libvulkan.so",
)

cc_library(
    name = "vulkan_linux",
    hdrs = glob([
        "include/vulkan/**/*.hpp",
        "include/vulkan/**/*.h",
    ]),
    strip_include_prefix = "include",
    visibility = ["//visibility:public"],
    deps = [":vulkan_linux_private"],
)
