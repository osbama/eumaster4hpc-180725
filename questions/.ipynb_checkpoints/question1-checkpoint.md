

## Order Matters

In this challenge question, you need to construct two circuits that perform two rotations on one qubit/wire and then measure the expectation value of the qml.PauliX quantum operator. The two circuits you need to implement are pictured in Figure 1.
![](q1.png)

Figure 1: The circuits you need to implement.
The provided template file order_matters_template.py contains a function compare_circuits that you need to complete. Specifically, the completed compare_circuits function should:

- Define a quantum device.
- Create two separate quantum functions that define the two circuits in Figure 1.
- Process the results from both circuits.

The circuits will do the following:

- Circuit 1: Rotate the qubit via the gate $R_{x}\left(\theta_{1}\right)$ (qml.RX) then via the gate $R_{y}\left(\theta_{2}\right)$ (qml.RY), then output $\left\langle\hat{\sigma}^{x}\right\rangle_{\text {circuit } 1}$ (using qml.expval(qml.PauliX(0))).
- Circuit 2: Rotate the qubit via the gate $R_{y}\left(\theta_{2}\right)$ (qml.RY) then via the gate $R_{x}\left(\theta_{1}\right) \quad(\mathrm{qml} . \mathrm{RX})$, then output $\left\langle\hat{\sigma}^{x}\right\rangle_{\text {circuit } 2}$ (using qml.expval(qml.PauliX(0))).

Make your compare_circuits function return the absolute value of the difference between the circuit outputs: $\left|\left\langle\hat{\sigma}^{x}\right\rangle_{\text {circuit } 1}-\left\langle\hat{\sigma}^{x}\right\rangle_{\text {circuit } 2}\right|$.

## Input

- list(float): The angles $\theta_{1}$ and $\theta_{2}$ in that order.


## Output

- float: The absolute value of the difference between the circuit outputs.

