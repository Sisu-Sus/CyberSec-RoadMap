# File System Operations: CREATE, READ, UPDATE, DELETE (CRUD)
## Introduction: The CRUD Cycle and File Management
The CREATE, READ, UPDATE, DELETE (CRUD) operations form the foundation of data management in virtually every software application. When applied to files, these operations define how programs interact with persistent storage. Understanding these operations is critical for both development and security auditing. This document will explore each operation within the context of file systems, highlighting potential vulnerabilities.

## CREATE: File Creation & Initialization
  - **Definition:** The `CREATE` operation establishes a new file on the file system.

  - **Technical Details:** This typically involves allocating disk space (or equivalent storage) and creating metadata entries that describe the file (name, size, permissions, timestamps). In programming languages like Python, this is often achieved using modes like "w" (write - overwrites existing files if they exist) or "x" (exclusive creation – fails if the file already exists).

  - **Example (Python)**:
   * ![CREATE Example In Python](images/crud_create.png)




### Next Steps
- [Troubleshooting](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Operating_Systems/Troubleshooting.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)


### Resource
- [https://www.crowdstrike.com/en-us/cybersecurity-101/observability/crud/](https://www.crowdstrike.com/en-us/cybersecurity-101/observability/crud/)
- [Python Documentation](https://docs.python.org/3/library/os.html)
