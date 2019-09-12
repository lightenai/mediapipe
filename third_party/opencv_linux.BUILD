# Description:
#   OpenCV libraries for video/image processing on Linux

licenses(["notice"])  # BSD license

exports_files(["LICENSE"])

# The following build rule assumes that OpenCV is installed by
# 'apt-get install libopencv-core-dev libopencv-highgui-dev \'
# '                libopencv-imgproc-dev libopencv-video-dev' on Debian/Ubuntu.
# If you install OpenCV separately, please modify the build rule accordingly.
cc_library(
    name = "opencv",
    srcs = glob(
        [
            "lib/libopencv_core.so.3*",
            "lib/libopencv_highgui.so.3*",
            "lib/libopencv_imgcodecs.so.3*",
            "lib/libopencv_imgproc.so.3*",
            "lib/libopencv_video.so.3*",
            "lib/libopencv_videoio.so.3*",
        ],
    ),
    hdrs = glob(["include/opencv2/**/*.h*"]),
    includes = ["include"],
    linkstatic = 1,
    visibility = ["//visibility:public"],
)
