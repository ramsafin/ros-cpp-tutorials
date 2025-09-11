FROM osrf/ros:noetic-desktop

RUN apt-get update && apt-get install -y --no-install-recommends \
  python3-catkin-tools \
  python3-rosdep \
  build-essential \
  git \
  && rm -rf /var/lib/apt/lists/*

RUN rosdep init || true
RUN rosdep update

ENTRYPOINT ["/ros_entrypoint.sh"]
CMD [ "/bin/bash" ]
