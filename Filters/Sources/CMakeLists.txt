set(Module_SRCS
  vtkArcSource.cxx
  vtkArrowSource.cxx
  vtkButtonSource.cxx
  vtkCellTypeSource.cxx
  vtkConeSource.cxx
  vtkCubeSource.cxx
  vtkCylinderSource.cxx
  vtkDiskSource.cxx
  vtkEllipseArcSource.cxx
  vtkEllipticalButtonSource.cxx
  vtkFrustumSource.cxx
  vtkGlyphSource2D.cxx
  vtkHyperTreeGridSource.cxx
  vtkLineSource.cxx
  vtkOutlineCornerFilter.cxx
  vtkOutlineCornerSource.cxx
  vtkOutlineSource.cxx
  vtkParametricFunctionSource.cxx
  vtkPlaneSource.cxx
  vtkPlatonicSolidSource.cxx
  vtkPointSource.cxx
  vtkPolyLineSource.cxx
  vtkProgrammableDataObjectSource.cxx
  vtkProgrammableSource.cxx
  vtkRandomHyperTreeGridSource.cxx
  vtkRectangularButtonSource.cxx
  vtkRegularPolygonSource.cxx
  #vtkRRandomTableSource.cxx # Should be in R kit
  #vtkSectorSource.cxx # Needs vtkRotationalExtrusionFilter
  vtkSelectionSource.cxx
  vtkSphereSource.cxx
  vtkSuperquadricSource.cxx
  vtkTessellatedBoxSource.cxx
  vtkTextSource.cxx
  vtkTexturedSphereSource.cxx
  vtkUniformHyperTreeGridSource.cxx
  vtkGraphToPolyData.cxx
  vtkDiagonalMatrixSource.cxx
  )

vtk_module_library(vtkFiltersSources ${Module_SRCS})
