# 🎁 JustRAIGS Challenge Pack 🎁

This Challenge Pack is a collection of JustRAIGS challenge codes and settings for IEEE ISBI 2024.

If you have any questions, feel free to reach out to me at yeganeh.madadi@gmail.com.


### ⚙️ Example algorithm ⚙️

An example algorithm container is provided via: ./example-algorithm.

You can study it and run it by calling:

    $ cd ./example-algorithm
    $ docker build --tag example-algorithm . && \
        rm -f test/output/* && \
        docker run --rm --gpus all \
        --volume $(pwd)/test/input:/input \
        --volume $(pwd)/test/output:/output \
        example-algorithm

This should output something along the lines of:

    =+==+==+==+==+==+==+==+==+==+=
    Torch CUDA is available: True
            number of devices: 1
            current device: 0
            properties: _CudaDeviceProperties(name='NVIDIA GeForce GTX 1650 Ti', major=7, minor=5, total_memory=4095MB, multi_processor_count=16)
    =+==+==+==+==+==+==+==+==+==+=
    Input Files:
    [PosixPath('/input/2332ec76-d9ba-437f-b03b-1fbebaf99401.mha')]
    De-Stacked /tmp/tmp0drsxkpw/image_1.png
    De-Stacked /tmp/tmp0drsxkpw/image_2.png
    De-Stacked /tmp/tmp0drsxkpw/image_3.png

You can prep it for upload using:

    $  docker save example-algorithm | gzip -c > example-algorithm.tar.gz


