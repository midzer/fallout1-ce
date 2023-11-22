# Emscripten

## Compile

```
mkdir build && cd build
emcmake cmake .. -DCMAKE_BUILD_TYPE=Release
emmake make
```

## Link

```
emcc -flto -O3 *.o game/*.o int/support/*.o int/*.o plib/*/*.o libfpattern.a -o index.html -sUSE_SDL=2 -sASYNCIFY -sINITIAL_MEMORY=768MB -sENVIRONMENT=web --preload-file fallout.cfg --preload-file f1_res.ini --preload-file CRITTER.DAT --preload-file MASTER.DAT --preload-file DATA/ --closure 1
```
