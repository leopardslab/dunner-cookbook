# Next.js SSR

This is a [Dunner](https://github.com/leopardslab/dunner) recipe for running your Next.js project (geared towards SSR) in a standardized Node environment.

## Usage

**Run the following command to initialize the Dunner recipe.**

```bash
$ dunner init next-js-ssr
```

This will go ahead and create the Dunner task file (`.dunner.yml`) required to execute Dunner commands.

## Commands

Prior to this, please specify any environment variables that your project uses in a .env file and in the Dunner task file. By default, this recipe will come with configuration for your authentication secret that you just have to specify the value for.

**Run the following to initialize the Next.js project directory.**

```bash
$ dunner do init
```

Run the following command to start the project in a production server

```bash
$ dunner do next start
```

Run the following command to build the application (does not start a server)

```bash
$ dunner do next build
```

Run the following to start the project in a development server

```bash
$ dunner do next
```

## Custom npm Scripts

You can execute the `next-custom` task in order to run any custom npm scripts that you have specified in your project:

```bash
$ dunner do next-custom INSERT_NAME_OF_SCRIPT
```
