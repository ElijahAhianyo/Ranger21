# Ranger21 Chebyshev Lr Functions

[_Documentation generated by Documatic_](https://www.documatic.com)

<!---Documatic-section-Codebase Structure-start--->
## Codebase Structure

<!---Documatic-block-system_architecture-start--->
```mermaid
None
```
<!---Documatic-block-system_architecture-end--->

# #
<!---Documatic-section-Codebase Structure-end--->

<!---Documatic-section-ranger21.chebyshev_lr_functions.cheb_steps-start--->
## ranger21.chebyshev_lr_functions.cheb_steps

<!---Documatic-section-cheb_steps-start--->
<!---Documatic-block-ranger21.chebyshev_lr_functions.cheb_steps-start--->
<details>
	<summary><code>ranger21.chebyshev_lr_functions.cheb_steps</code> code snippet</summary>

```python
def cheb_steps(m, M, T):
    (C, R) = ((M + m) / 2.0, (M - m) / 2.0)
    thetas = (np.arange(T) + 0.5) / T * np.pi
    return 1.0 / (C - R * np.cos(thetas))
```
</details>
<!---Documatic-block-ranger21.chebyshev_lr_functions.cheb_steps-end--->
<!---Documatic-section-cheb_steps-end--->

# #
<!---Documatic-section-ranger21.chebyshev_lr_functions.cheb_steps-end--->

<!---Documatic-section-ranger21.chebyshev_lr_functions.cheb_perm-start--->
## ranger21.chebyshev_lr_functions.cheb_perm

<!---Documatic-section-cheb_perm-start--->
<!---Documatic-block-ranger21.chebyshev_lr_functions.cheb_perm-start--->
<details>
	<summary><code>ranger21.chebyshev_lr_functions.cheb_perm</code> code snippet</summary>

```python
def cheb_perm(T):
    perm = np.array([0])
    while len(perm) < T:
        perm = np.vstack([perm, 2 * len(perm) - 1 - perm]).T.flatten()
    return perm
```
</details>
<!---Documatic-block-ranger21.chebyshev_lr_functions.cheb_perm-end--->
<!---Documatic-section-cheb_perm-end--->

# #
<!---Documatic-section-ranger21.chebyshev_lr_functions.cheb_perm-end--->

[_Documentation generated by Documatic_](https://www.documatic.com)