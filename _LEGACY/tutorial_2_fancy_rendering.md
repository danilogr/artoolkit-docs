# ARToolkit Tutorial 2: Fancy Rendering

## Introduction

A commonly-asked questions by users new to ARToolKit, is "How can I draw (insert name of some visually wild concept) on a marker instead of this dumb cube?". The answer to this question is actually outside the scope of ARToolKit, since ARToolKit only sets up the drawing coordinate system inside OpenGL.. it does not try to address drawing of models itself. However, in order to use plain OpenGL drawing, or some external rendering library to render fancy drawing on top of your markers, you will need to know where to make changes to an application based on the typical ARToolKit samples. This following sections of this tutorial will show you how.

For users looking for a high quality renderer to pair with ARToolKit, we have developed [osgART][1]: ARToolKit for OpenSceneGraph. OpenSceneGraph (OSG) is a modern, well-supported and highly capable renderer, and ARToolKit's video acquisition and tracking can be seamlessly merged into the scene-graph rendering of OSG via the [osgART][1] library. OSG provides high-quality rendering in an OpenGL-friendly environment, with an extensible plugin architecture allowing a huge variety of rendering techniques to be used. Using osgART requires use of different application structure and techniques to the standard ARToolKit examples, and some knowledge of C++ (whereas ARToolKit is purely C-based). The extra investment in learning how to use osgART pays off very quickly however, as everything that can be accomplished with ARToolKit can be easily embedded into applications sporting the huge power of OSG. osgART is the path-to rapid development of high-quality AR and MR applications.

If you are interested in the scene-graph based approach to AR applications offered by osgART, we suggest you switch to reading the [osgART documentation][1].

If using osgART isn't an option for you, the standard ARToolKit does include support for one external rendering library: OpenVRML. Although [VRML][2] is not usually associated with visually-realistic 3D content, it is flexible and well-supported by many 3D toolsets. [OpenVRML][3] provides an open-source parser and renderer for VRML97 and X3D files, including support for texturing, animation and networked content, and is supported on a variety of platforms including Windows, Mac OS X (through the [Fink package manager][4]) and Linux (through the [Debian package system][5]).

[1]: /osgART
[2]: http://en.wikipedia.org/wiki/VRML
[3]: http://www.openvrml.org
[4]: http://pdb.finkproject.org/pdb/search.php?summary=openvrml
[5]: http://packages.debian.org/src:openvrml