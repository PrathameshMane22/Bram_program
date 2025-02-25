import numpy as np

N = 256  # Number of samples
angles = np.linspace(0, 2 * np.pi, N, endpoint=False)
sine_values = np.round(127 * np.sin(angles)).astype(int)
cosine_values = np.round(127 * np.cos(angles)).astype(int)

# Save as Verilog memory file
with open("sine_lut.coe", "w") as f:
    f.write("memory_initialization_radix=10;\n")
    f.write("memory_initialization_vector=\n")
    f.write(",\n".join(map(str, sine_values)) + ";")

with open("cosine_lut.coe", "w") as f:
    f.write("memory_initialization_radix=10;\n")
    f.write("memory_initialization_vector=\n")
    f.write(",\n".join(map(str, cosine_values)) + ";")

print("LUT files generated!")
