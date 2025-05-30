load("//xla/tsl:tsl.bzl", "internal_visibility")
load("//xla/tsl:tsl.default.bzl", "get_compatible_with_portable")
load("//xla/tsl/platform:rules_cc.bzl", "cc_library")

package(
    # copybara:uncomment default_applicable_licenses = ["//tensorflow:license"],
    default_visibility = ["//visibility:public"],
    features = [
        # Required since headers are not self-contained.
        "-parse_headers",
    ],
    licenses = ["notice"],
)

cc_library(
    name = "fixedpoint",
    hdrs = [
        "FixedPoint.h",
        "MatMatProduct.h",
        "MatMatProductAVX2.h",
        "MatMatProductNEON.h",
        "MatVecProduct.h",
        "PacketMathAVX.h",
        "PacketMathAVX2.h",
        "PacketMathAVX512.h",
        "TypeCastingAVX2.h",
        "TypeCastingAVX512.h",
    ],
    compatible_with = get_compatible_with_portable(),
    deps = [
        "//xla/tsl/framework:fixedpoint_types",
        "@eigen_archive//:eigen3",
    ],
)

filegroup(
    name = "xla_cpu_runtime_hdrs",
    srcs = [
        "FixedPoint.h",
        "MatMatProduct.h",
        "MatMatProductAVX2.h",
        "MatMatProductNEON.h",
        "MatVecProduct.h",
        "PacketMathAVX.h",
        "PacketMathAVX2.h",
        "PacketMathAVX512.h",
        "TypeCastingAVX2.h",
        "TypeCastingAVX512.h",
    ],
    compatible_with = get_compatible_with_portable(),
    visibility = internal_visibility([
        "//tensorflow:__subpackages__",
        "//xla/tsl:internal",
    ]),
)

# Files needed for core:mobile_srcs_no_runtime.
filegroup(
    name = "mobile_srcs_only_runtime",
    srcs = [
        "FixedPoint.h",
        "MatMatProduct.h",
        "MatMatProductAVX2.h",
        "MatMatProductNEON.h",
        "MatVecProduct.h",
        "PacketMathAVX.h",
        "PacketMathAVX2.h",
        "PacketMathAVX512.h",
        "TypeCastingAVX2.h",
        "TypeCastingAVX512.h",
    ],
    compatible_with = get_compatible_with_portable(),
)

filegroup(
    name = "mobile_srcs_no_runtime",
    srcs = [
        "FixedPoint.h",
        "MatMatProduct.h",
        "MatMatProductAVX2.h",
        "MatMatProductNEON.h",
        "MatVecProduct.h",
        "PacketMathAVX.h",
        "PacketMathAVX2.h",
        "PacketMathAVX512.h",
        "TypeCastingAVX2.h",
        "TypeCastingAVX512.h",
    ],
    compatible_with = get_compatible_with_portable(),
)
