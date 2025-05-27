Download link : https://programming.engineering/product/com-sgn-110-exercise-11/

COM-SGN.110 EXERCISE 11
The tasks should be completed and presented to TA during the lab session. Do not forget to upload your solutions to Moodle! Questions about exercises should be addressed to the TA personally, through Moodle messages or via email, which can be found on the Moodle page of the course.

    YUV to RGB transformation

        Load the file yuvdata.mat to the MATLAB workspace. Note the sizes of the variables and compare them to the given dimensions of the image (rows*cols). Is there a difference? Why/why not?

        Reshape the components yy, uu and vv to the given image size (reshape), upsampling as necessary (imresize). Display the components in a 1×3 subplot to verify the result.

        Center the U and V components around zero by subtracting 127 (note the data type).

        Flatten and concatenate the components for conversion to RGB:

YUV=cat(2,Y(:),U(:),V(:)).

        Perform the transformation from YUV to RGB with the matrix given above:

RGB=YuvToRgb*YUV’.

        Reshape each component back to the image size and produce the RGB image. Show the result via imshow.

    Chrominance subsampling

        Load the RGB image lena.tiff and convert it to YCbCr colorspace (use built-in function rgb2ycbcr). Display Y, Cb and Cr in a 1×3 subplot.

        Perform subsampling of the chrominance components, following each of the formats described in the lecture material: 4:2:2, 4:1:1, 4:2:0. Separately also perform subsampling on the luminance component, following the format 4:1:1. (Hint: you can use MATLAB indexing with a given step size to avoid for-loops.)

        Upsample the same components back to the original resolution (imresize), recombine them and convert the images back to RGB (ycbcr2rgb). Show the five RGB images (the original and 4 subsampled ones) together on a subplot. Is there a perceptible difference?

        Calculate the mean squared error values of the subsampled images with respect to the original (immse). Does the result support your previous conclusion?



