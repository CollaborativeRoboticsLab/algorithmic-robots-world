FROM ros:jazzy

# Install rviz2
RUN apt-get update && \
	apt-get install -y \
        ros-jazzy-rviz2 \
        x11-apps \
	&& rm -rf /var/lib/apt/lists/*

# Set up environment for X11
ENV DISPLAY=:0
ENV QT_X11_NO_MITSHM=1

ENTRYPOINT [ "/ros_entrypoint.sh" ]

