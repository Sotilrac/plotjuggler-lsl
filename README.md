# PlotJuggler Lab Streaming Layer plugin

This repository contains a streaming plugin for
[PlotJuggler](https://github.com/facontidavide/PlotJuggler) that
uses the Lab Streaming Layer.

You can find additional information about LSL here: https://labstreaminglayer.readthedocs.io/info/intro.html

## Build
To build this plugin, PlotJuggler must be installed in your system.

On Linux, perform a full compilation and installation:

### Install Dependencies (Linux Only)
```bash
sudo apt install -y qtbase5-dev libqt5svg5-dev libqt5websockets5-dev \
      libqt5opengl5-dev libqt5x11extras5-dev libprotoc-dev libzmq3-dev \
      liblz4-dev libzstd-dev
```

### Build and Install Plot Juggler
```
git clone https://github.com/facontidavide/PlotJuggler.git
cd PlotJuggler
mkdir build; cd build
cmake ..
make
sudo make install
```

### Compile this plugin
```
git clone --recurse-submodules https://github.com/Sotilrac/plotjuggler-lsl.git
cd plotjuggler-lsl
mkdir build; cd build
cmake -DPlotJuggler_LIBRARY:FILEPATH="/usr/local/bin/" ..
make
sudo make install
```

### Compile this plugin (for Windows):

**Windows Installer**:
[PlotJuggler-Windows-3.9.0-installer](https://github.com/facontidavide/PlotJuggler/releases/download/3.9.0/PlotJuggler-Windows-3.9.0-installer.exe)

```
git clone --recurse-submodules https://github.com/Sotilrac/plotjuggler-lsl.git
cd plotjuggler-lsl
mkdir build; cd build
cmake -DPlotJuggler_LIBRARY:FILEPATH="C:/YOURPATH/PlotJuggler/build/lib" -DPlotJuggler_INCLUDE_DIR:FILEPATH="C:/YOURPATH/PlotJuggler/plotjuggler_base/include" ..
make
sudo make install
```

## Plugin installation

If PlotJuggler can't find this plugin, check the folder where the file
`libDataStreamLSL.so` is located and add it manually in:

    App -> Preferences... -> Plugins

Code contributed by: 

- Celal Savur (@csavur)
- Shitij Kumar (@spk4422)
- Mazin Ali (@mazinms)
