Running in MATLAB 2020b

1.CCSDS_Near_Loss_Encode.p
 Input parameters:
   - imagePath: Path to the input image directory (string)
   - outputDir: Directory to store the output file (string)
   - Nx: Image width (integer)
   - Ny: Image height (integer)
   - Nz: Number of spectral bands (integer)
   - near:Peak Absolute Error (PAE) (integer) 
   - sample_encoding_order: Pixel arrangement order, 0: BIL (band interleaved by line), 1: BSQ (band sequential)
   - large_d: Bit depth, 12, 14, or 16
   - Byte_Order: Byte endianness, 0: Big-endian, 1: Little-endian

Example:
CCSDS_Near_Loss_Encode("imagePath", "outputDir", 512, 512, 5, 0, 0, 12, 1);

2.CCSDS_Near_Loss_Decode.p
 Input parameters:
   - input_code: Directory containing the input code stream (string)
   - output_image: Directory to store the output image (string)
   - Nx: Image width (integer)
   - Ny: Image height (integer)
   - Nz: Number of spectral bands (integer)
   - near: Peak Absolute Error(PAE) (integer) 
   - large_d: Bit depth, 12, 14, or 16
Example:
CCSDS_Near_Loss_Decode("input_code", "output_image", 512, 512, 5, 0,12);

 Fixed parameters (not user-specified):
   -- large_r: 64
   -- large_omega: 19
   -- prediction_mode: Full prediction
   -- local_sum_type: Wide local sum
   -- v_min: -6
   -- v_max: 4
   -- weight_initialization_method: Default initialization
   -- gamma_star: 8
   -- gamma_0: 1
   -- large_p: 4
   -- large_theta: 0
% For detailed explanations of the parameters, refer to the original standard CCSDS-123.0-B-2.
