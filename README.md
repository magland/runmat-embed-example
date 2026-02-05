> ⚠️ **Early Stage & Experimental** - This project is in early development and should be considered experimental.

# RunMat Embed Example

This repository demonstrates how to embed interactive MATLAB scripts in Markdown files using [runmat-embed](https://github.com/magland/runmat-embed). When rendered on GitHub Pages, the embedded scripts become editable and executable directly in the browser via [RunMat](https://runmat.org).

## Example

* **Rendered**: [example1](https://magland.github.io/runmat-embed-example/example1)
* **Source**: [example1.md](https://raw.githubusercontent.com/magland/runmat-embed-example/refs/heads/main/example1.md)

```markdown
<script src="https://magland.github.io/runmat-embed/runmat-embed.js"></script>

This demonstrates how to embed RunMat in a markdown file that can be rendered on GitHub pages.

<runmat-embed>
<iframe width="100%" height="600" frameborder="0"></iframe>
<script type="text/plain" class="matlab-script">
% Matrix operations example
A = [8, 1, 6; 3, 5, 7; 4, 9, 2];  % Example matrix
disp('Matrix A:')
disp(A)

disp('Sum of each row:')
disp(sum(A, 2))

disp('Sum of each column:')
disp(sum(A, 1))

disp('Sum of diagonal:')
disp(sum(diag(A)))

disp('Total sum:')
disp(sum(sum(A)))
</script>
</runmat-embed>

If it worked, you should see an embedded RunMat above with a matrix operations example.

Here's another example with numerical integration:

<runmat-embed>
<iframe width="100%" height="600" frameborder="0"></iframe>
<script type="text/plain" class="matlab-script">
% Numerical integration using trapezoidal rule
a = 0;
b = pi;
n = 100;

% Create evenly spaced points
h = (b - a) / (n - 1);
x = a:h:b;
y = sin(x);

% Trapezoidal rule: (h/2) * (y(1) + 2*sum(y(2:end-1)) + y(end))
integral_approx = (h/2) * (y(1) + 2*sum(y(2:end-1)) + y(end));

disp(['Approximate integral of sin(x) from 0 to pi: ', num2str(integral_approx)])
disp('Exact value: 2')
disp(['Error: ', num2str(abs(integral_approx - 2))])
</script>
</runmat-embed>
```

## Additional Resources

For more ways to embed RunMat via runmat-embed in websites, see the [runmat-embed examples](https://github.com/magland/runmat-embed/tree/main/examples).
