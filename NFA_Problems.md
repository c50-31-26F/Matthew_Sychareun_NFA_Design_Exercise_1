# NFA Submission

## NFA Problem 8: [ {string s| s starts with 01 and ends with 10 } ]

![NFA 8 Diagram](NFA_Problem_8.jpg)

<table>
  <tr>
    <th align="center"><h3>Test strings</h3></th>
    <th align="center"><h3>Hand-Drawn Tree Computation</h3></th>
  </tr>
  <tr>
    <td align="center"><img src="NFA_Problem_8_Test.png" alt="NFA 8 Tests" width="700"></td>
    <td align="center"><img src="NFA_Problem_8_Tree.png" alt="NFA 8 Tree" width="800" height="480"></td>
  </tr>
</table>

<table>
  <tr>
    <th align="left" colspan="3"><h3>Step-by-Step State Transitions (Input: 01110)</h3></th>
  </tr>
  <tr>
    <th align="center">Start</th>
    <th align="center">Step 1: q0 reads <code>0</code> → move to q1</th>
    <th align="center">Step 2: q1 reads <code>1</code> → branches to q2 and q3</th>
  </tr>
  <tr>
    <td align="center"><img src="nfa8_step_start.jpg" alt="Start" width="500"></td>
    <td align="center"><img src="nfa8_step_one.jpg" alt="Step 1" width="500"></td>
    <td align="center"><img src="nfa8_step_two.jpg" alt="Step 2" width="500"></td>
  </tr>
</table>

<table>
  <tr>
    <th align="left">Step 3: read 1</th>
    <th align="left">Step 4: read 1</th>
    <th align="left">Step 5: read 0</th>
    <th align="left">Step 6: Input finished</th>
  </tr>
  <tr>
    <td align="center"><img src="nfa8_step_three.jpg" alt="Step 3" width="500"></td>
    <td align="center"><img src="nfa8_step_four.jpg" alt="Step 4" width="500"></td>
    <td align="center"><img src="nfa8_step_five.jpg" alt="Step 5" width="500"></td>
    <td align="center"><img src="nfa8_step_six.jpg" alt="Step 6" width="500"></td>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li><b>Branch A (q2):</b> read <code>1</code> → branch into q2 and q3</li>
        <li><b>Branch B (q3):</b> read <code>1</code> → no transition (dies)</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>Branch A (q2):</b> read <code>1</code> → branch into q2 and q3</li>
        <li><b>Branch B (q3):</b> read <code>1</code> → no transition (dies)</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>Branch A (q2):</b> read <code>0</code> → stay in q2</li>
        <li><b>Branch B (q3):</b> read <code>0</code> → move to q4</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>Branch A (q2):</b> not accepting → Reject</li>
        <li><b>Branch B (q4):</b> accepting → Accept</li>
      </ul>
    </td>
  </tr>
</table>

## NFA Problem 11: [ {string s | the 2nd to last bit is 1}]

![NFA 11 Diagram](NFA_Problem_11.jpg)

<table>
  <tr>
    <th align="center"><h3>Test strings</h3></th>
    <th align="center"><h3>Hand-Drawn Tree Computation</h3></th>
  </tr>
  <tr>
    <td align="center"><img src="NFA_Problem_11_Test.jpg" alt="NFA 11 Tests" width="700"></td>
    <td align="center"><img src="NFA_Problem_11_Tree.png" alt="NFA 11 Tree" width="800" height="480"></td>
  </tr>
</table>

<table>
  <tr>
    <th align="left" colspan="3"><h3>Step-by-Step State Transitions (Input: 0111)</h3></th>
  </tr>
  <tr>
    <th align="center">Start</th>
    <th align="center">Step 1: q0 reads <code>0</code> → stay in q0</th>
    <th align="center">Step 2: q0 reads <code>1</code> → branches to q0 and q1</th>
  </tr>
  <tr>
    <td align="center"><img src="nfa11_start.jpg" alt="Start" width="500"></td>
    <td align="center"><img src="nfa11_step_one.jpg" alt="Step 1" width="500"></td>
    <td align="center"><img src="nfa11_step_two.jpg" alt="Step 2" width="500"></td>
  </tr>
</table>

<table>
  <tr>
    <th align="left">Step 3: read 1</th>
    <th align="left">Step 4: read 1 (last symbol)</th>
    <th align="left">Step 5: Input finished</th>
  </tr>
  <tr>
    <td align="center"><img src="nfa11_step_three.jpg" alt="Step 3" width="500"></td>
    <td align="center"><img src="nfa11_step_four.jpg" alt="Step 4" width="500"></td>
    <td align="center"><img src="nfa11_step_five.jpg" alt="Step 5" width="500"></td>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li><b>Branch A (q0):</b> read <code>1</code> → branch into q0 and q1</li>
        <li><b>Branch B (q1):</b> read <code>1</code> → move to q2</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>Branch A (q0):</b> read <code>1</code> → branch into q0 and q1</li>
        <li><b>Branch B (q1):</b> read <code>1</code> → move to q2</li>
        <li><b>Branch C (q2):</b> read <code>1</code> → no transition (dies)</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>q0:</b> not accepting → Reject</li>
        <li><b>q1:</b> not accepting → Reject</li>
        <li><b>q2 (from Branch B):</b> accepting → Accept</li>
      </ul>
    </td>
  </tr>
</table>


## NFA Problem 12: [ {string s | s contains exactly 3 1's}]

![NFA 12 Diagram](NFA_Problem_12.jpg)

<table>
  <tr>
    <th align="center"><h3>Test strings</h3></th>
    <th align="center"><h3>Hand-Drawn Tree Computation</h3></th>
  </tr>
  <tr>
    <td align="center"><img src="NFA_Problem_12_Test.jpg" alt="NFA 12 Tests" width="700"></td>
    <td align="center"><img src="NFA_Problem_12_Tree.png" alt="NFA 12 Tree" width="800" height="480"></td>
  </tr>
</table>

<table>
  <tr>
    <th align="left" colspan="3"><h3>Step-by-Step State Transitions (Input: 10101)</h3></th>
  </tr>
  <tr>
    <th align="center">Start</th>
    <th align="center">Step 1: q0 reads <code>1</code> → move to q1</th>
    <th align="center">Step 2: q1 reads <code>0</code> → stay in q1</th>
  </tr>
  <tr>
    <td align="center"><img src="nfa12_start.jpg" alt="Start" width="500"></td>
    <td align="center"><img src="nfa12_step_one.jpg" alt="Step 1" width="500"></td>
    <td align="center"><img src="nfa12_step_two.jpg" alt="Step 2" width="500"></td>
  </tr>
</table>

<table>
  <tr>
    <th align="left">Step 3: q1 reads <code>1</code> → move to q2</th>
    <th align="left">Step 4: q2 reads <code>0</code> → stay in q2</th>
    <th align="left">Step 5: q2 reads <code>1</code> → move to q3</th>
  </tr>
  <tr>
    <td align="center"><img src="nfa12_step_three.jpg" alt="Step 3" width="500"></td>
    <td align="center"><img src="nfa12_step_four.jpg" alt="Step 4" width="500"></td>
    <td align="center"><img src="nfa12_step_six.jpg" alt="Step 5: input finished" width="500"></td>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li>Only one path, so no branching</li>
        <li>Second <code>1</code> read</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li>Only one path, so no branching</li>
        <li>One symbol left to read</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li>Third <code>1</code> read</li>
        <li>Input finished in <b>q3</b> (accepting) → Accept</li>
      </ul>
    </td>
  </tr>
</table>

## NFA Problem 23: [ {string s | s has odd length or s =01 }]

![NFA 23 Diagram](NFA_Problem_23.jpg)

<table>
  <tr>
    <th align="center"><h3>Test strings</h3></th>
    <th align="center"><h3>Hand-Drawn Tree Computation</h3></th>
  </tr>
  <tr>
    <td align="center"><img src="NFA_Problem_23_Test.jpg" alt="NFA 23 Tests" width="700"></td>
    <td align="center"><img src="NFA_Problem_23_Tree.png" alt="NFA 23 Tree" width="800" height="480"></td>
  </tr>
</table>

<table>
  <tr>
    <th align="left" colspan="2"><h3>Step-by-Step State Transitions (Input: 010)</h3></th>
  </tr>
  <tr>
    <th align="center">Start: q0 takes λ-moves to q1 and q4</th>
    <th align="center">Step 1: read <code>0</code></th>
  </tr>
  <tr>
    <td align="center"><img src="nfa23_start.jpg" alt="Start" width="500"></td>
    <td align="center"><img src="nfa23_step_one.jpg" alt="Step 1" width="500"></td>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li><b>Branch A (q1):</b> q0 follows λ to q1 without reading input</li>
        <li><b>Branch B (q4):</b> q0 follows λ to q4 without reading input</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>q0:</b> no transition on <code>0</code> (dies)</li>
        <li><b>Branch A (q1):</b> read <code>0</code> → move to q2</li>
        <li><b>Branch B (q4):</b> read <code>0</code> → move to q5</li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <tr>
    <th align="center">Step 2: read <code>1</code></th>
    <th align="center">Step 3: read <code>0</code> (input finished)</th>
  </tr>
  <tr>
    <td align="center"><img src="nfa23_step_two.jpg" alt="Step 2" width="500"></td>
    <td align="center"><img src="nfa23_step_three.jpg" alt="Step 3" width="500"></td>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li><b>Branch A (q2):</b> read <code>1</code> → move to q3</li>
        <li><b>Branch B (q5):</b> read <code>1</code> → move to q4</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>Branch A (q3):</b> read <code>0</code> → no transition (dies)</li>
        <li><b>Branch B (q4):</b> read <code>0</code> → move to <b>q5</b> (accepting) → Accept</li>
      </ul>
    </td>
  </tr>
</table>

## NFA Problem 24: [ {string s | s has odd number of 0's or s = 001}]

![NFA 24 diagram](NFA_Problem_24.jpg)

<table>
  <tr>
    <th align="center"><h3>Test strings</h3></th>
    <th align="center"><h3>Hand-Drawn Tree Computation</h3></th>
  </tr>
  <tr>
    <td align="center"><img src="NFA_Problem_24_Test.jpg" alt="NFA 24 Tests" width="700"></td>
    <td align="center"><img src="NFA_Problem_24_Tree.png" alt="NFA 24 Tree" width="800" height="480"></td>
  </tr>
</table>

<table>
  <tr>
    <th align="left" colspan="3"><h3>Step-by-Step State Transitions (Input: 0010)</h3></th>
  </tr>
  <tr>
    <th align="center">Start: q0 takes λ-moves to q1 and q5</th>
    <th align="center">Step 1: read <code>0</code></th>
    <th align="center">Step 2: read <code>0</code></th>
  </tr>
  <tr>
    <td align="center"><img src="nfa24_start.jpg" alt="Start" width="500"></td>
    <td align="center"><img src="nfa24_step_one.jpg" alt="Step 1" width="500"></td>
    <td align="center"><img src="nfa24_step_two.jpg" alt="Step 2" width="500"></td>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li><b>Branch A (q1):</b> q0 follows λ to q1 without reading input</li>
        <li><b>Branch B (q5):</b> q0 follows λ to q5 without reading input</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>q0:</b> no transition on <code>0</code> (dies)</li>
        <li><b>Branch A (q1):</b> read <code>0</code> → move to q2</li>
        <li><b>Branch B (q5):</b> read <code>0</code> → move to q6</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>Branch A (q2):</b> read <code>0</code> → move to q3</li>
        <li><b>Branch B (q6):</b> read <code>0</code> → move to q5</li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <tr>
    <th align="center">Step 3: read <code>1</code></th>
    <th align="center">Step 4: read <code>0</code> (input finished)</th>
  </tr>
  <tr>
    <td align="center"><img src="nfa24_step_three.jpg" alt="Step 3" width="500"></td>
    <td align="center"><img src="nfa24_step_four.jpg" alt="Step 4" width="500"></td>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li><b>Branch A (q3):</b> read <code>1</code> → move to q4</li>
        <li><b>Branch B (q5):</b> read <code>1</code> → stay in q5</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><b>Branch A (q4):</b> read <code>0</code> → no transition (dies)</li>
        <li><b>Branch B (q5):</b> read <code>0</code> → move to <b>q6</b> (accepting) → Accept</li>
      </ul>
    </td>
  </tr>
</table>
