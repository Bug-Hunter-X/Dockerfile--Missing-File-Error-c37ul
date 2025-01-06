# Dockerfile Bug: Missing File Error

This repository demonstrates a common error in Dockerfiles where the build process fails due to a missing file or directory. The error message from Docker is often not very informative, making it difficult to diagnose the problem.

## Bug Description

The provided Dockerfile attempts to run a Python script, `/app/my_script.py`. However, this script is not included in the Dockerfile's context, leading to a runtime error. The error message from Docker might mention a missing file or directory but won't explicitly state `/app/my_script.py` is the culprit. 

## Solution

The solution involves explicitly copying the required files into the image using the `COPY` instruction.  The fixed Dockerfile includes the necessary script.
