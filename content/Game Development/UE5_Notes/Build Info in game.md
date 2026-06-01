# Build.cs

```cpp
using System.Diagnostics;  
using System.IO;  
using UnrealBuildTool;  
  
public class GAME : ModuleRules  
        try  
        {  
            string gitHash = RunGit("rev-parse --short HEAD") ?? "unknown";  
            string gitDate = RunGit("show -s --format=%cI HEAD") ?? "unknown";  
  
            string genDir = Path.Combine(ModuleDirectory, "BuildInfo");  
            if (!Directory.Exists(genDir)) Directory.CreateDirectory(genDir);  
            string genPath = Path.Combine(genDir, "GitBuildInfo.gen.h");  
  
            string content = "#pragma once\n\n"  
                             + $"#define ZENIO_GIT_COMMIT_HASH TEXT(\"{gitHash}\")\n"  
                             + $"#define ZENIO_GIT_COMMIT_DATE TEXT(\"{gitDate}\")\n";  
  
            if (!File.Exists(genPath) || File.ReadAllText(genPath) != content)  
            {  
                File.WriteAllText(genPath, content);  
            }  
        }  
        catch  
        {  
            // ignore; fall back to unknown if anything fails  
        }  
    }  
  
    private string RunGit(string arguments)  
    {  
        try  
        {  
            var psi = new ProcessStartInfo("git", arguments)  
            {  
                UseShellExecute = false,  
                RedirectStandardOutput = true,  
                CreateNoWindow = true,  
                WorkingDirectory = ModuleDirectory  
            };  
            using (var p = Process.Start(psi))  
            {  
                if (p == null) return null;  
                p.WaitForExit(2000);  
                return p.StandardOutput.ReadToEnd().Trim();  
            }  
        }  
        catch  
        {  
            return null;  
        }  
    }  
}
```

In .cpp: declare UFUNCTIONS that grab the generated macro (from this build.cs) and use it in game.