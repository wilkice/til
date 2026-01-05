1. view GC settings for this JVM: `jcmd <pid> GC.heap_info`. this is used for newer JDK. For older JDK such as JDK 8, should use `jmap -heap <pid>`. And should notice that the jmap output is more readable.
2. use `jcmd <pid> VM.flags` to show JVM parameters, so that we can know which collector is using.
3. use `jstat -gcutil <pid> 5s` to view gc info.