# minecraft folder path

Get the location of the user's `.minecraft` directory.

Based on a [JavaScript library](https://github.com/simonmeusel/minecraft-folder-path) of the same name.

This is primarily useful if you want to cache Minecraft-related data in the user's default Minecraft directory.
Note that they may have multiple `.minecraft` directories, or it may be somewhere else if they configured it to be.

```rs
// Windows: `%appdata%.minecraft`
// Mac: `$HOME/Library/Application Support/minecraft`
// Linux: `$HOME/.minecraft`
if let Some(minecraft_dir) = minecraft_folder_path::minecraft_dir() {
    println!("{minecraft_dir}");
}
```
