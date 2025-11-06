# mean-and-variance

# MEAN-VARIANCE-AND-CROSS-CORRELATION

## Aim
To write a program for mean, variance, and cross-correlation in Scilab and verify the output.

## Equipment Needed

1.Computer with i3 Processor

2.Scilab Software

## Algorithm

1.Start.

2.Define function f(x) = 2*x.

3.Set integration limits a = 0, b = 1.

4.Compute mean of X: integrate x*f(x) over [a, b].

5.Compute E[X²]: integrate x²*f(x) over [a, b].

6.Compute variance of X: VarX = EX2 - EX^2.

7.Display EX (mean) and VarX (variance).

8.Input reference sequence x_seq and second sequence y_seq.

9.Compute sequence lengths n1 and n2.

10.Compute cross-correlation r = corr(x_seq, y_seq, n1).

11.Plot cross-correlation using plot2d3.

12.End.

## Procedure

1.Refer to the algorithm and understand the steps of the experiment.

2.Open Scilab on your system.

3.Type your code in a new editor window.

4.Save the file with an appropriate name.

5.Execute the code by pressing F5 or using the Execute option.

6.If any errors occur, check your code, correct them, and execute again.

7.When the code runs successfully, input the sequences for cross-correlation when prompted.

8.Verify the generated results:

9.Mean of X

10.Variance of X

11.Cross-correlation plot

12. Analyze the results as per your experiment’s requirement.
## Program
```
clc;
clear;

deff('y=f(x)', 'y = 2*x'); 

a = 0;
b = 1;

deff('y=g(x)', 'y = x*f(x)');
EX = intg(a, b, g);
deff('y=h(x)', 'y = x^2*f(x)');
EX2 = intg(a, b, h);
VarX = EX2 - EX^2;

disp(EX, "Mean of X =");
disp(VarX, "Variance of X =");


x_seq = input("Type in the reference sequence (X) = "); 
y_seq = input("Type in the second sequence (Y) = "); 

n1 = max(size(y_seq)) - 1;
n2 = max(size(x_seq)) - 1;

r = corr(x_seq, y_seq, n1);

plot2d3('gnn', r);

```

### Output

![WhatsApp Image 2025-11-06 at 09 36 00_134f26e7](https://github.com/user-attachments/assets/56e271b8-2027-4ba5-843a-cb858b718a19)

![WhatsApp Image 2025-11-06 at 09 35 46_83cf3291](https://github.com/user-attachments/assets/f83a7ddd-180b-42c3-a21f-202aa11c6d78)


### Tabular Column:


![WhatsApp Image 2025-11-06 at 09 45 39_483976a7](https://github.com/user-attachments/assets/f984ed25-e111-425b-a1ed-2bcf31c25906)


### MANUAL CALCULATION:


![Uploading WhatsApp Image 2025-11-06 at 09.45.38_e0479c7c.jpg…]()




### RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
