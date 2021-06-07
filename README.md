# ICSSgen3D v1.0
![](ICSSgen3D_icon_full.png)

Developed by Zhe Wang, Hiroshima University.

**Homepage** https://www.wangzhe95.net

ICSSgen3D can help you creating input files for 3D-ICSS calculation.

## Update Histroy
### v1.0.0 (2021-06-06)
First release of ICSSgen3D, please enjoy!

## Usage
*For more details information, please refer to the user manual.*
1. Run ICSSgen3D. Python 3.9 IDE is needed.
2. Prepare an original input file. An example of input file is shown below. You could find this 
input file in the *example* folder.

```
%nprocshared=6
%mem=10GB
%chk=methylazulene.chk
#p nmr=giao rb3lyp/6-31g(d)

optimized_1-methylazulene

0 1
 C                 -2.68122300   -0.69593600    0.00002600
 ...
 
```
3. Specify the original input file path, you can darg the input file to
the command window. Then, press ENTER key.
```
Please specify the original input file path:
(e.g.: /ICSSgen3D/example/methylazulene.gjf)
(User input) /Users/tetsu/Desktop/methylazulene.gjf 
```
4. Next, you need to specify the size of calculation space. Please specify the range
of X, Y, Z axis one by one.
```
Please specify the range of X axis (in angstrom, e.g., -10 10):
(User input) -7.5 7.5

Please specify the range of Y axis (in angstrom, e.g., -8 8):
(User input) -6.5 6.5

Please specify the range of Z axis (in angstrom, e.g., -8 8):
(User input)-6 6

3D-ICSS map in [X: -7.5 to 7.5, Y: -6.5 to 6.5, Z: -6.0 to 6.0].
```
5. Specify the grid quailty of 3D-ICSS calculation. The default value is 0.25, you can press
ENTER key to use the default value.
```
Please specify the grid quality:
(press Enter to use default value 0.25)
(User input) (ENTER)
ICSSgen3D will use grid quality of 0.25.
```
6. Several input files named as *xxx_3DICSS_00xx.gjf* would be generated to the same dictionary with the original input file.
Please submit this input files to *Gaussian* calculation. 
**Tips:** You can use [RunGJF](https://github.com/wongzit/minorScripts) for submitting automatically.
