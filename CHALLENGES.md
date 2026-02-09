# Challenges Faced and Solutions

During the implementation of this project, I faced several technical challenges. These helped me understand DevOps tools more deeply.

## 1. Docker Not Recognized on Local System
Initially, Docker commands were not recognized on my system.
- **Cause:** Docker Desktop was not installed or running.
- **Solution:** Installed Docker Desktop and verified installation using `docker --version`.

## 2. Application Not Accessible from Browser
After running the container, the application was not accessible.
- **Cause:** Incorrect port mapping while running Docker container.
- **Solution:** Corrected the Docker run command to map port `3000:3000`.

## 3. GitHub Push Errors Due to Large Files
GitHub rejected the push due to large Terraform provider files.
- **Cause:** `.terraform` and `node_modules` directories were committed.
- **Solution:** Added these directories to `.gitignore` and removed them from Git tracking.

These challenges helped me understand real-world DevOps issues and how to troubleshoot them effectively.
