# Rails Dynamic `render` Path Traversal

- What it is: User-controlled template names passed directly to Rails `render` can make Rails search unintended filesystem paths.
- Look for parameters such as `template` that directly influence what view is rendered.
- Historical vulnerable pattern:
```ruby
render params[:template]
```
- The book describes encoded absolute-path input:
```text
template=%2fetc%2fpasswd
```
- Vulnerable Rails behavior searched `/app/views`, the application root, then the server root.
- Use a non-sensitive known test file where possible; `/etc/passwd` is presented in the book as a conventional proof.
- False positive: modern patched Rails or explicit view allowlists stop the traversal.
- Edge case: file permissions and render-mode configuration determine what can be read.
- Remediation: update Rails and map user choices to fixed server-side template identifiers.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
