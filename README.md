# FEAL_KEM: CPU-based Parallel Library for Electromagentic Finite Element Solver
The finite element method (FEM) has the advantage of not being limited by the geometric shape of the analysis structure because it provides various types of elements, and can define material constants for each element. This is a discrete technique essential for numerical analysis of large complex shapes and composite material structures. Unlike the method of moments (MoM), a representative numerical analysis technique that uses only the surface information of the structure when analyzing electromagnetic fields, FEM discretizes the internal/external regions of the structure. In addition, the methodology of calculating the characteristics of unit elements and then combining the characteristics of all elements requires large-scale calculations in the global matrix assembly process involving repeated operations of similar processes. In this study, we developed a numerical library for the MPI-based domain partitioning technique by utilizing METIS, a graph partitioning-based parallel library that divides a large analysis domain into subdomains and assigns operations in the subdomains to each processor.

Most electromagnetic analysis problems on 3D complex structures (especially in the high-frequency region) are computationally very large, depending on the size of the computational space and the accuracy of the calculation. These huge FEM algebraic systems require a large amount of storage space and a powerful linear solver. In this lab, we have developed a numerical library capable of efficient large-scale parallel calculations by utilizing MUMPS, a parallel computation library based on the multi-frontal technique.

# MPI implementation in FEAL_AEM 1.0
In FEAL_AEM 1.0, MPI parallelization is implemented using MPI. MPI-related features are as follows:

# Authors
+ Hyesun Na (hyesunna@yonsei.ac.kr), School of Mathematics and Computing(Computational Science and Engineering), Yonsei University (v1.0)

+ Youngmin Shin (youngmm@yonsei.ac.kr), School of Mathematics and Computing(Computational Science and Engineering), Yonsei University (v1.0)

+ Eunjung Lee (eunjunglee@yonsei.ac.kr), School of Mathematics and Computing(Computational Science and Engineering), Yonsei University (v1.0)


# Usage
## Downloading FEAL_AEM

## Compile
### Prerequisites
Prerequisites to compile FEAL_AEM are as follows:
+ MPI
+ METIS
+ MUMPS
+ eigen-3.4.0
+ libigl
+ Compiler(we should)

### Compile and build
+ Build FEAL_AEM

+ Build an example problem after build FEAL_AEM

+ Build all

## Mores on compile option

### Running the example

# Folder structure
+ `src` : source files of FEAL_AEM 1.0.
+ `example` : source files of an example problem for 3D vector-wave equation.
+ `include` : header files are created after building.
+ `lib` : a static library of FEAL_AEM 1.0 is are created after building
+ `doc` : documentation
+ `run` : an executable binary file for the example problem is created after building.
+ `tool` : contains useful scripts and tools.

# Cite
Please use the following bibtex, when you refer to this project.
```
@misc{FEAL_AEM2024,
    title  = "Parallel Library for Electrocmagnetic Finite Element Solver",
    author = "Shin, Younming-min and Na, Hye-Sun and Lee, Eun-Jung",
    url    = "https://github.com/FEAL-Lab/FEAL_AEM",
    year   = "2024"
}
```

# References


