# Awesome cv - CMake build template

This project is meant to be a quick start template to write your own [Awesome CV](https://github.com/posquit0/Awesome-CV)
locally using Cmake and making use of the great cmake module [UseLatex](https://gitlab.kitware.com/kmorel/UseLATEX).

For more infos check out the documentation of UseLATEX [here](https://gitlab.kitware.com/kmorel/UseLATEX/).

## Quick start

To quickly build the `.tex` files into the relative pdf run
```shell
mkdir build
cd build
cmake ..
make cv # other targets: resume, coverletter
```
The `target-name.pdf` file will be located in the `build/` directory.

### UseLatex module update

If any change in the upstream Cmake module [UseLatex.cmake](UseLATEX.cmake) is detected(the Github [Action](.github/workflows/update-cmake-module.yml)
runs monthly[^1]) a new Pull Request will be opened.

## License

This project is licensed under the [MIT LICENSE](LICENSE).

---
[^1]: You can also manually trigger an update with a manual dispatch if you need. 

