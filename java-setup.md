# Download and Setup Java

## Steps

1. [Download Java](https://www.java.com/en/download/).

2. Download one or more [OpenJDK builds from Oracle](https://jdk.java.net/).

3. Open the Terminal and switch into the downloads directory:

   ```sh
   cd Downloads
   ```

4. Use the `ls` command to identify each archived JDK file that was downloaded.

5. Run the following command to unarchive each file:

```sh
tar -xf file-name.tar.gz
```

7. Switch the root directory, `cd ~`, then type `ls Library/J` and press the tab key to output the autocomplete suggestions.

   Verify that the directory path `Library/Java/JavaVirtualMachines` exists.

   If not, create the folders using `mkdir Library/Java` and `mkdir Library/Java/JavaVirtualMachines`.

8. Switch back to `cd Downloads`, and move each unarchived folder into `~/Library/Java/JavaVirtualMachines/`.

   For example, if the name of the unarchived folder is `jdk-23.0.2.jdk`, run the following command:

   ```sh
   mv jdk-23.0.2.jdk ~/Library/Java/JavaVirtualMachines/jdk-23.0.2.jdk
   ```

9. Switch to the root directory, `cd ~`, then use the following command to list all available Java Virtual Machine versions:

   ```sh
   /usr/libexec/java_home -V
   ```

   **Sample Output**

   ```sh
   Matching Java Virtual Machines (3):
     23.0.2 (x86_64) "Oracle Corporation" - "OpenJDK 23.0.2" /Library/Java/JavaVirtualMachines/jdk-23.0.2.jdk/Contents/Home
     17.0.14 (x86_64) "Amazon.com Inc." - "Amazon Corretto 17" /Library/Java/JavaVirtualMachines/amazon-corretto-17.jdk/Contents/Home
     1.8.441.07 (x86_64) "Oracle Corporation" - "Java" /Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home
   ```

10. Select the desired version by setting it to the `JAVA_HOME` environment variable.

    For example, if the selected Java Virtual Machine is `17.0.14 (x86_64) "Amazon.com Inc." - "Amazon Corretto 17"`:

    ```sh
    export JAVA_HOME=$(/usr/libexec/java_home -v 17.0.14)
    ```

    If the same version is frequently used, consider exporting the above variable as a script inside the `.zshrc` or `.bashrc` file.

11. Verify that the desired Java version has been selected:

    ```sh
    java -version
    ```
