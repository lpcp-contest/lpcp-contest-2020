# Fighting with the gang of Billy the Kid

*(The original description from the previous edition can be found [here](https://github.com/lpcp-contest/lpcp-contest-2019/blob/master/billykid/billykid.md).)*

Sheriff Pat is determined to fight with Billy the Kid and his gang.
In order to catch the gang he wants to locate his men, whom he trusts, to several towns in New Mexico so that when he visits one of these towns he can get intelligence about the gang.
He wants to be sure that during any of his travels in New Mexico visiting N towns (without any revisit to a town) he finds at least one among these N towns where he has located a man from his team.
His aim is to choose minimum number of towns for locating his men considering the human resources in his team.


## Input format

The first line contains three integers, `T`, `C` and `N`, the number of towns and connections in the instance, and the length of travels.
The following `C` lines contain two integers each, `A` and `B`, meaning that town `A` is connected to town `B` (and vice versa).
Towns are indexed from `1` to `N`.


## Output format

In the first line you need to write `S`, the number of selected towns.
In the second line you need to write the selected towns, in increasing order and separated by space.


## Example

Instance:

```
6 7 3
1 4
1 2
2 3
3 4
3 5
4 5
5 6
```

SHA-1 of the expected output: `3d333362ef6db5366276cfad59dbe735989d8abb`

Characters in the expected output: `6`

Output:

```
2
3 4
```

Solution [here](https://github.com/alviano/lpcp-contest-2020/raw/master/billykid.zip).
We used a BASH script combining Python scripts for processing input and output, and `clingo` to actually solve the problem.
We produced the output file with the following command:
```
$ solve.sh <instance.0.in >instance.0.out
```
and we could check our solution before submission with the following commands:
```sh
$ sha1sum instance.0.out 
3d333362ef6db5366276cfad59dbe735989d8abb  instance.0.out
$ wc -c instance.0.out 
6 instance.0.out
```