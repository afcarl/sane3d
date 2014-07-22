sane3d
======

Since I was really disappointed with the overly complicated 3D plotting interface of matplotlib, I decided to write a easier interaface ffor my everyday work. It mainly generates the `meshgrid` data, needed by matplotlib, automatically. So if you have 2D data, that you want to plot as surface, you can simply write

    z = generate_my_2d_data()
    sane3d.plot_matrix_surface(z)
    
The same works for `scatter`, `wireframe`, `contour` and `contourf`.

If you want to scale the axis, you can additionally give the axis tics as `Array`s

    z = generate_my_2d_data()
    x = np.linspace(-10, 20, z.shape[0])
    y = np.linspace(-1, 2, z.shape[1])
    sane3d.plot_matrix_surface(x, y, z)
    
All additional parameters are handed to the original plotting function. Thus the following will work as expected.

    sane3d.plot_matrix_surface(z, cstride=10, rstride=20)
    
I also put a [notebook](http://nbviewer.ipython.org/github/hildensia/sane3d/blob/master/doc/Sane3D%20test.ipynb), reproducing all of the [mplot3d tutorial](http://matplotlib.org/mpl_toolkits/mplot3d/tutorial.html) examples online.
    
