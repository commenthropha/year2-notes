- A more modular design achieved through the separation of different layers
- Bottom layer is the hardware and the top layer is the user
- Layer k uses the service of layer k-1 and provides service to layer k+1
### Advantages
- Simplicity of construction
- Ease of debugging
- Clear interfaces between layers
### Disadvantages
- Defining layers is difficult
- May be less efficient as system calls access multiple layers to execute which adds overhead