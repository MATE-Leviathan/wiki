# Intro to using HoloOcean

## Configuration

The package should be called **Leviathan** and the scenario **MorgantonPool**.

## Example Usage

An example make command would look like:

```python
with holoocean.make("MorgantonPool") as env:
    # Your code here
```

## Known Issues

* **Collision Mesh Accuracy**: The collision mesh of the pool is not accurate. This should be fixed when importing new pool parts.
* **Pool Boundary**: There is no limit on the top of the pool, allowing the ROV to escape. Adding an invisible collision plane/box should resolve this.

