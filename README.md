# C++ build code for sublime text-3

```
{
    //"shell_cmd": "g++ -std=c++11 -Wall \"${file}\" -o \"${file_path}/${file_base_name}\" && \"${file_path}/${file_base_name}\"",
    "cmd" : ["g++ -std=c++17 $file_name -o $file_base_name && timeout 30s ./$file_base_name<in.txt>out.txt"],
    // "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
    "working_dir": "${file_path}",
    "selector": "source.c++, source.cpp, source.cc, source.cxx",
    //"name": "Run in Terminal",

    "variants":
    [
        {
            "name": "Run in Terminal",

            "linux": {
                "cmd" : ["g++ -std=c++17 -std=c++14 -Wall -Wextra -pedantic -O2 -Wshadow -Wformat=2 -Wfloat-equal -Wconversion -Wlogical-op -Wshift-overflow=2 -Wduplicated-cond -Wcast-qual -Wcast-align -D_GLIBCXX_DEBUG -D_GLIBCXX_DEBUG_PEDANTIC -D_FORTIFY_SOURCE=2 -lmcheck -fsanitize=undefined -fno-sanitize-recover -fstack-protector $file_name -o $file_base_name && timeout 20s ./$file_base_name<in.txt>out.txt"],
            },
            "shell": true,
        },
    ]
}
```

Go to `tools->build system-> new build system` and then copy and paste the code and then just select the build system. build code with ctrl+B, user `Run in terminal` option and you'll be fine.
