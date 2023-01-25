# Setup for NSight Debugging

1. Follow the README.md to setup SSH with VSCode

2. SSH into vscode-dsmlp

https://user-images.githubusercontent.com/43923184/153686245-2dcb6006-36df-483f-93e6-60d1e6d0e208.mov

3. Install the required plugins - Nvidia Nsight extension and the C/C++ extension

https://user-images.githubusercontent.com/43923184/153686284-ce2b83de-ba14-437a-b5b7-9d244db723fd.mov

4. Open up the launch.json file and paste the following contents

(Replace the program with the path to the binary file generated by the make command and the argument field with any of the test cases)

```
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "CUDA C++: Launch",
            "type": "cuda-gdb",
            "request": "launch",
            "gdb": "cuda-gdb",
            "program": "/home/rchandan/cse160-WI22/PA2/solution",
            "arguments": ["-e /home/rchandan/cse160-WI22/PA2/Dataset/0/output.raw -i /home/rchandan/cse160-WI22/PA2/Dataset/0/input1.raw,/home/rchandan/cse160-WI22/PA2/Dataset/0/input1.raw -t vector"]
        }
    ]
}
```

https://user-images.githubusercontent.com/43923184/153686371-f7c2b5a7-277b-4265-b4e2-3d32112938d3.mov

5. Add breakpoints in your file from which you generated the binary and run with debugging

https://user-images.githubusercontent.com/43923184/153686736-4f7c25bf-738e-480a-982c-f71774720482.mov


Stay tuned for a Discussion section for more on using the NSight debugger!


