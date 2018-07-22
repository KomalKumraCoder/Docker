# Docker
Differences between containers and images
• An image is a read-only filesystem.
• A container is an encapsulated set of processes running in a read-write
copy of that filesystem.
• To optimize container boot time, copy-on-write is used instead of regular
copy.
• docker run starts a container from a given image
Creating the first images
There is a special empty image called scratch.
• It allows to build from scratch.
The docker import command loads a tarball into Docker.
• The imported tarball becomes a standalone image.
• That new image has a single layer.
Creating other images
docker commit
• Saves all the changes made to a container into a new layer.
• Creates a new image (effectively a copy of the container).
docker build
• Performs a repeatable build sequence.
• This is the preferred method!
