# Hello Loopback4 on Glitch
====================================================
[https://glitch.com/~hello-loopback4](https://glitch.com/~hello-loopback4)
- LoopBack 4, the next step in the evolution of LoopBack! A completely redesigned modular framework especially for API developers. 

- Follow the Loopback 4 tutorial using [this Glitch project!](https://glitch.com/~hello-loopback4)

- Following instructions at loopback v4 page [http://v4.loopback.io/getting-started.html](http://v4.loopback.io/getting-started.html)

====================================================

1. [done] install Node.js 
2. [done] installed loopback version 4 using the following command:

```
pnpm install --save-dev @loopback/cli
```

### Next Create a new Loopback4 project

3. To create a new project, run the CLI as follow

- First, open the Glitch console ![](https://cdn.glitch.com/f6c8cc1d-327c-4f33-a27c-5c97e3954ae2%2FGlitchOpenConsole.png?1538522618760)

- Type the following command the console

    ```
    lb4 app
    ```

- Answer the prompts as follows.

    ```
    [?] Project name: hello-loopback4
    [?] Project description: hello-loopback4
    [?] Project root directory: hello-loopback4
    [?] Application class name: HelloApplication
    [?] Select project build settings: Enable tslint, Enable prettier, Enable mocha, Enable loopbackBuild
    ```
    
    ![Choose features](https://cdn.glitch.com/f6c8cc1d-327c-4f33-a27c-5c97e3954ae2%2FglitchLoopback4Two.png?1538524133848)
    ![e.g.](https://cdn.glitch.com/f6c8cc1d-327c-4f33-a27c-5c97e3954ae2%2FGlitchLoopback4-first.png?1538521335992)

### Move the LB project files into the Glitch root
    
- Move and edit the lb4 generated project files

    ```
    # move the lb4 generated project files
    mv ./hello-loopback4/README.md ./README-hello-loopback4.md

    # reference the generated README from this Glitch README
    sed -i '$a\
    [README-hello-loopback4](./README-hello-loopback4.md)' README.md

    mv ./hello-loopback4/{.[!.],}* .
    rm -r ./hello-loopback4

    # update to node version 10
    sed -i 's/>=8.9/10.x/' ./package.json

    # Sync Glitch console with the Glitch project
    refresh
    ```
    
### Starting the project

4. The project comes with a "ping" route to test the project. Let's try it out by running the projects.

- Wait for Glitch project to finish rebuilding
- In a browser, visit http://hello-loopback4.glitch.me:3000/ping


### Continue...

