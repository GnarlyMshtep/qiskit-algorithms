Here are some things to explore if we can do better: 
- noise profiling: 
    - a few different links on Piazza
    - may be simulating with the wrong noise 
    - https://piazza.com/class/kxs8ssff32d2fk?cid=272_f4
    - the IBM machine supports some gate set, the noise model that we currently have seemingly only adds noise to those gates. 
    - the compilation that we did 
    - ```python  
        result = execute(circ, Aer.get_backend('qasm_simulator'),
                 coupling_map=coupling_map,
                 basis_gates=basis_gates,
                 noise_model=noise_model).result()
    ```
        - partiuclarly the `basis_gates` line
        - `coupling_map=coupling_map` restricts u to the IBM's 5-qubits (prob not needed)
        -  try on a complex circuit
- The reuslts were still consistent with the basic theory that regular simulator is perfect while noisy sim isn't and is between the perfect simulator and an actual machine. 
- https://quantum-computing.ibm.com/
- Try to run on different simulators & different machines and see if there are different results. 
- we used Qeato
- only base algorithms are implemented. 
- the qiskit qubit ordering is reveresed, so have to U-f backward
    - `reversed(range(n + 1))`
- look at the report, not the code, see what you can add. 
- in terms of the report, adding more actual data 
- add some statistics. 
- a table is one run. 
- *more results for QAOA and shor*
- *the shor section is lacking*

From augeste answer
-  explain how your solution with enough detail that a competent programmer could reimplement the internal behavior of your code. This doesn't require implementation specific details or actual code unless they are particularly illustrative or interesting. 
    - add section of how to 
    - orcale construction: Copy paste from jacob email
    - meaningfull choices: running for a 1024, 
    - issues: 
    - perhaps going into predicting the 