This project is intended to make possible the use of OpenCL in Delphi and Free Pascal (Lazarus).

Authors:
  * niello **Site: http://www.niello.org.ua**<br></li></ul>

<ul><li>Igroman <b>Site: <a href='http://Igroman14.livejournal.com'>http://Igroman14.livejournal.com</a></b><br>
What OpenCL platforms / Operating Systems / Compilers are supported? <br></li></ul>

OpenCL Platforms:<br>
<ul><li>tested on AMD, Nvidia <br>
</li><li>if you are running on a different platform, please contact us <br>
Operating Systems:<br>
</li><li>Windows XP, Windows Vista, Windows 7 <br>
</li><li>Code for Linux added but not tested <br>
</li><li>if you are running on a different OS, please contact us <br>
Compilers:<br>
</li><li>Delphi (6, 7, 2010, XE2) <br>
</li><li>FPC (2.2.0, 2.4.2) <br>
</li><li>if you are running on a different compiler, please contact us <br></li></ul>

How do I get the Source Code? <br>
The project repository is located on svn. Latest development version always can be downloaded using svn. <br>
You can copy source code: <br>
<ul><li>svn checkout <a href='http://delphi-opencl.googlecode.com/svn/'>http://delphi-opencl.googlecode.com/svn/</a> <br>
How to use it? <br>
</li><li>CL, CL_platforms, CL_GL, CL_d3d9, cl_d3d10, cld3d11, cldx9_media_sharing, cl_ext, cl_gl_ext (.pas) a OpenCL headers for Pascal compilers. <br>
</li><li>OpenCL (.inc) - are include file for them. <br>
</li><li>DelphiCL (.pas) - OOP classes for OpenCL. <br>
</li><li>DelphiCL (.inc) - are include file for them. (LOGGING for logging in file "DELPHI_LOG.log", PROFILING for profiling). <br>
</li><li>oclUtils (.pas) - don't use this. (Depercated) <br>
</li><li>Samples (Sample1-Sample5) - samples of using on OpenCL in Delphi and Free Pascal. <br></li></ul>

Before using the <b>TDCLClasses</b>, need execute procedure: <br>
<pre><code><br>
InitOpenCL();// default library name = OpenCL.dll for Windows, libOpenCL.so for Linux<br>
</code></pre>
if you are using CL_GL sharing, need added InitCL_GL() procedure: <br>
<pre><code><br>
InitCL_GL();<br>
</code></pre>

The TDCLPlatforms allow get access to the all platforms on the computer (AMD, NVidia, Intel etc.). <br>
You need to create specimen of this class: <br>
<pre><code><br>
var<br>
platforms: TDCLPlatforms;<br>
...<br>
begin<br>
platforms := TDCLPlatforms.Create();<br>
//Your code here<br>
FreeAndNil(platforms);<br>
end;<br>
</code></pre>

The <b>TDCLPlatforms</b> have property Platforms (Array of <b>PDCLPlatform</b> - Pointer to the <b>TDCLPlatform</b>). <br>
More in the source files. <br>
Maybe later we'll write a more detailed guide. <br>