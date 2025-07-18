In this challenge question, you need to construct two circuits that perform two
rotations on one qubit/wire and then measure the expectation value of the
qml.PauliXquantum operator. The two circuits you need to implement are
pictured in Figure 1.

The provided template contains a function
`compare_circuits` that you need to complete. Specifically, the completed
compare_circuitsfunction should:

- Define a quantum device.


- Create two separate quantum functions that define the two circuits in
    Figure 1.
- Process the results from both circuits.

The circuits will do the following:

- Circuit 1: Rotate the qubit via the gate _Rx_ ( _θ_ 1 ) (qml.RX) then
    via the gate _Ry_ ( _θ_ 2 ) (qml.RY), then output 〈 _σ_ ˆ _x_ 〉circuit 1 (using
       qml.expval(qml.PauliX(0))).
- Circuit 2: Rotate the qubit via the gate _Ry_ ( _θ_ 2 ) (qml.RY) then
    via the gate _Rx_ ( _θ_ 1 ) (qml.RX), then output 〈 _σ_ ˆ _x_ 〉circuit 2 (using
       qml.expval(qml.PauliX(0))).
Make yourcompare_circuitsfunction return the absolute value of the difference
between the circuit outputs:|〈ˆ _σx_ 〉circuit 1−〈ˆ _σx_ 〉circuit 2|.

```
Input
```
- list(float): The angles _θ_ 1 and _θ_ 2 in that order.

```
Output
```
- float: The absolute value of the difference between the circuit outputs.

```
