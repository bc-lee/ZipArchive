load("@rules_cc//cc:defs.bzl", "objc_library")

package(default_visibility = ["//visibility:public"])

objc_library(
    name = "ZipArchive",
    srcs = glob([
        "SSZipArchive/**/*.c",
        "SSZipArchive/minizip/**/*.h",
        "SSZipArchive/**/*.m",
    ]),
    hdrs = glob([
        "SSZipArchive/SSZipArchive.h",
        "SSZipArchive/SSZipCommon.h",
        "SSZipArchive/include/ZipArchive.h",
    ]),
    defines = [
        "HAVE_ARC4RANDOM_BUF",
        "HAVE_ICONV",
        "HAVE_INTTYPES_H",
        "HAVE_PKCRYPT",
        "HAVE_STDINT_H",
        "HAVE_WZAES",
        "HAVE_ZLIB",
        "ZLIB_COMPAT",
    ],
    enable_modules = True,
    includes = [
        "SSZipArchive",
        "SSZipArchive/include",
        "SSZipArchive/minizip",
    ],
    module_name = "ZipArchive",
    sdk_dylibs = [
        "z",
        "iconv",
    ],
    sdk_frameworks = [
        "Security",
    ],
)
