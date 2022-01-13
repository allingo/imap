## Imap
Imap is a tool for visualize the hd-map. This project was inspired by Apollo.
```
data     // hd-map dir
main.py  // main process
map.py  // hd-map struct
editor.py  // user interaction
```

## Quick start
#### dependency
The following is the tested environment, python3 is also feasible, but I did not test.
```
Python      2.7.17
matplotlib  2.2.5
protobuf    3.17.3
```
If you encounter problems, you can try uninstalling and then reinstalling to ensure that the software version is consistent.

#### Install
There are 2 ways to install imap.
1. Install matplotlib and protobuf.
```
pip install -U matplotlib
pip install protobuf
```

2. Or you can install conda first, then install protobuf. Use `conda install protobuf` to install will fail, I haven't found the reason yet. Replace with the following command will work.
```
pip install protobuf
```

## Example
After the installation is complete, you can view the map with the following command.
```
python main.py -m data/borregas_ave.txt
```

The following is the display of the hd-map in `data\borregas_ave.txt`.You can click on the lane you want to display more detail info, which will display the current lane's id, as well as the predecessor and successor lane's id in the upper left corner.

![map_show](doc/img/map_show.jpg)

## Questions
1. After running the command `python main.py -m data/your_map_file.bin`, nothing display and no errors!!!
A: Check the permissions of the map file, if the current user does not have permissions, modify the permissions with the following commands.
```
sudo chmod 777 data/your_map_file.bin
```

## Todo
1. add argparse.ArgumentParser
2. show map in more details (like layers, styles)  // now
3. select lane to convert color
