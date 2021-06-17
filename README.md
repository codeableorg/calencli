# CalenCLI

> Before starting!
>
> 1. Create a new folder with the project name and open it from VS Code
>
> 2. From the VS Code terminal run the next docker command
>
> ```powershell
> docker container run \
> --name ruby \
> -it \
> -v $(pwd):/app \
> -v ssh:/root/.ssh \
> -v bundle:/usr/local/bundle \
> -e GIT_USER_NAME=<your_username> \
> -e GIT_USER_EMAIL=<your_email> \
> --rm \
> codeableorg/ruby
> ```
>
> 3. Clone the repository of your work team
>
> ```powershell
> $ git clone git@github.com:codeableorg/calencli-c4w1-xxx.git .
> ```
>
> 4.  Run some initialization scripts
>
> ```powershell
> $ bootstrap
> ```
>
> 5.  Install some necessary gems for rubocop to work properly
>
> ```powershell
> $ bundle install
> ```
>
> ready, you can work on your project!

Looking for the project instructions? Find them on [this doc](https://www.notion.so/ableco/CalenCLI-458b56a674d446dcbd59e831a5b6e4a9)

To disable temporarily any Rubocop convention:

```
# rubocop:disable Metrics/AbcSize
def complex_and_irreducible_method(that, receive, a, lot, of, params)
  ...
  ...
  ...
end
# rubocop:enable Metrics/AbcSize
```

To disable them, use the convention that Rubocop is complaining about. _Metrics/AbcSize_ is just an example.

Modify `calencli.rb`. You can create as many files as you want but `calencli.rb` should be the main one.

After commit your changes, push you changes to your Github repo.
