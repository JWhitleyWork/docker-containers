FROM jwhitleywork/ros:foxy-ros-base-focal

# install ros packages
RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-foxy-action-tutorials-cpp \
    ros-foxy-action-tutorials-interfaces \
    ros-foxy-action-tutorials-py \
    ros-foxy-angles \
    ros-foxy-composition \
    ros-foxy-demo-nodes-cpp \
    ros-foxy-demo-nodes-cpp-native \
    ros-foxy-demo-nodes-py \
#    ros-foxy-depthimage-to-laserscan \
    ros-foxy-dummy-map-server \
    ros-foxy-dummy-robot-bringup \
    ros-foxy-dummy-sensors \
    ros-foxy-examples-rclcpp-minimal-action-client \
    ros-foxy-examples-rclcpp-minimal-action-server \
    ros-foxy-examples-rclcpp-minimal-client \
    ros-foxy-examples-rclcpp-minimal-composition \
    ros-foxy-examples-rclcpp-minimal-publisher \
    ros-foxy-examples-rclcpp-minimal-service \
    ros-foxy-examples-rclcpp-minimal-subscriber \
    ros-foxy-examples-rclcpp-minimal-timer \
    ros-foxy-examples-rclpy-executors \
    ros-foxy-examples-rclpy-minimal-action-client \
    ros-foxy-examples-rclpy-minimal-action-server \
    ros-foxy-examples-rclpy-minimal-client \
    ros-foxy-examples-rclpy-minimal-publisher \
    ros-foxy-examples-rclpy-minimal-service \
    ros-foxy-examples-rclpy-minimal-subscriber \
    ros-foxy-image-tools \
    ros-foxy-intra-process-demo \
    ros-foxy-joy \
    ros-foxy-lifecycle \
    ros-foxy-logging-demo \
    ros-foxy-pcl-conversions \
    ros-foxy-pendulum-control \
    ros-foxy-pendulum-msgs \
#    ros-foxy-quality-of-service-demo-cpp \
    ros-foxy-quality-of-service-demo-py \
    ros-foxy-ros-workspace \
#    ros-foxy-rqt-common-plugins \
    ros-foxy-rviz-default-plugins \
    ros-foxy-rviz2 \
    ros-foxy-teleop-twist-joy \
    ros-foxy-teleop-twist-keyboard \
    ros-foxy-tlsf \
    ros-foxy-tlsf-cpp \
    ros-foxy-topic-monitor \
    && rm -rf /var/lib/apt/lists/*
