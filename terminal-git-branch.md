# How to Display the Current Git Branch from the Terminal

## Steps

1. Open the Terminal and switch to the root folder:

   ```sh
   cd ~
   ```

2. Next, ensure that the appropriate Unix shell configuration file has been created.

   If using Z shell:

   ```sh
   cat .zshrc
   ```

   If using Bash

   ```sh
   cat .bashrc
   ```

   If the following log is returned, create the file using `touch <filename>`.

   ```
   cat: <file name>: No such file or directory
   ```

3. Open the configuration file:

   If using nano:

   ```sh
   nano <file name>
   ```

   If using Vim:

   ```sh
   vi <file name>
   ```

4. Add the following code in the file:

   ```sh
   function parse_git_branch() {
      git branch 2> /dev/null | sed -n -e 's/^\* \(.*\)/(\1)/p'
   }

   COLOR_DEF=$'%f'
   COLOR_USR=$'%F{243}'
   COLOR_DIR=$'%F{197}'
   COLOR_GIT=$'%F{39}'
   setopt PROMPT_SUBST
   export PROMPT='${COLOR_DIR}%c ${COLOR_GIT}$(parse_git_branch)${COLOR_DEF} $ '
   ```

   To save and exit using nano: `ctrl` + `o`, `enter`, `ctrl` + `x`

   To edit using Vim, press `i`.

   To save and exit using Vim: `esc`, `:wq`, `enter`

5. To load the new script, start a new Terminal session by opening another window or tab.

6. Verify by switching to another directory with Git initialized.
