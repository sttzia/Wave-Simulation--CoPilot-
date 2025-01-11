# Wave Simulation

This repository contains a Python implementation of a wave simulation. The simulation models the propagation of waves through different media and visualizes the results as a video.

## Clone Repository

To clone this repository, use the following command:

```bash
git clone https://github.com/sttzia/Wave-Simulation--CoPilot-
```

## Installation

To run the wave simulation, you need to install the following dependencies:

- numpy
- imageio
- matplotlib
- imageio-ffmpeg

You can install these dependencies using pip:

```bash
pip install numpy imageio matplotlib imageio-ffmpeg
```

## Code Explanation

### main.py

The main script contains the implementation of the wave simulation. Below is a brief explanation of the key components:

- **wave_simulation_AI class**: This class encapsulates all the simulation methods.

  - `__init__(self, dx_in, dt_in, sz_x_in, sz_y_in, steps_in, broadcast_func_in)`: Constructor to initialize the simulation parameters.
  - `Laplace(self, u_array, dx)`: Computes the Laplace operator used in the wave equation.
  - `Edge_detect(self, c_array)`: Simple edge detector for identifying steps in the refractive index.
  - `run(self)`: Executes the simulation and generates the output video.

- **broadcast functions**: These functions define different scenarios for wave propagation.
  - `broadcast_func_lin_wave(t)`: Simulates a plane wave through a material with high refractive index.
  - `broadcast_func_prism_wave(t)`: Simulates a plane wave through a prism.
  - `broadcast_func_circlular_lens(t)`: Simulates a plane wave through a circular lens.
  - `broadcast_func_fresnel(t)`: Simulates a plane wave through a Fresnel lens.
  - `broadcast_func_blazed_grading(t)`: Simulates a plane wave through a blazed grating.
  - `broadcast_func_phased_antenna_streight(t)`: Simulates a plane wave through a phased antenna array.
  - `broadcast_func_phased_antenna_angle(t)`: Simulates a plane wave through a phased antenna array at an angle.
  - `broadcast_func_phased_antenna_focus(t)`: Simulates a plane wave through a phased antenna array with focus.
  - `broadcast_func_phased_antenna_focus2(t)`: Simulates a plane wave through a phased antenna array with a different focus.
  - `broadcast_func_radar(t)`: Simulates a plane wave through a radar system.
  - `broadcast_func_image(t)`: Simulates a plane wave through an image-based waveguide.

### Running the Simulation

To run the simulation, execute the `main.py` script:

```bash
python main.py
```

This will generate a video file named `Waveguide.mp4` that visualizes the wave propagation.

### Modifying the .bmp Images

The simulation uses two .bmp images; one of them is to define the waveguide. You can modify these images to change the waveguide's structure:

- **Waveguide.bmp**: This image defines the waveguide's structure. The blue channel of the image is used to set the refractive index of the waveguide. You can edit this image using any image editing software.

### Output Video File

The output video file `Waveguide.mp4` visualizes the wave propagation through the waveguide. The red and green channels represent the positive and negative displacements of the wave, respectively. The blue channel highlights the waveguide's structure and edges.

### Simulation Steps

The variable `steps = 10000` defines the number of time steps in the simulation. Increasing this value will result in a longer simulation and a longer output video. However, it will also increase the computation time.

### Warning: Time Computation

Running the simulation with `steps = 10000` can take a significant amount of time, potentially exceeding half an hour!. Ensure that you have sufficient computational resources and time before running the simulation.

Use `steps = 100` for a test `Waveguide.mp4` output file, of approximately `3 seconds` first!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
