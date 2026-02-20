1.Demo Video
https://youtu.be/-w9VlFIIsRY

2.Reflection Questions
i.What are the main differences between a Docker image and a Docker container?
A Docker Image is a read-only, static template containing the application code, libraries, and environment configurations required for execution. In contrast, a Docker Container is a live, executable instance of an image. Using an OOP analogy, an image is the class (blueprint), while the container is the object (runtime instance).

ii.Explain how Docker's layered architecture improves efficiency.
Docker utilizes a Union File System (UnionFS) where images are constructed from a series of stackable, immutable layers. This improves efficiency through layer sharing; if multiple images share the same base layer (e.g., Ubuntu or Python), Docker stores that layer only once. This significantly reduces disk space consumption and accelerates image transfers by only moving the unique, modified layers.

iii.Why does each container get its own writable layer?
When a container starts, Docker adds a thin, ephemeral writable layer (the "container layer") on top of the read-only image layers. This ensures that any file modifications or temporary data generated during execution are isolated to that specific container. Because the underlying image layers remain untouched, the same image can be safely shared by multiple concurrent containers.

iv.What are the benefits of using Docker Compose over running containers individually?
Docker Compose simplifies the management of multi-container applications by defining them in a single docker-compose.yml configuration file. It provides declarative orchestration, allowing you to start, stop, and scale complex environments (comprised of web servers, databases, and caches) with a single command. This ensures consistent networking and volume configuration across development, testing, and production environments.
