cmake_minimum_required(VERSION 3.21)
project(rtcuda CUDA)

set(CMAKE_CUDA_STANDARD 14)

add_executable(rtcuda main.cu vec3.cuh ray.cuh primitive.cuh camera.cuh hit_record.cuh material.cuh utility.cuh)

set_target_properties(rtcuda PROPERTIES
        CUDA_ARCHITECTURES "50;75")