^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package moveit_ros_perception
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

2.14.0 (2025-06-13)
-------------------

2.13.2 (2025-04-16)
-------------------

2.13.1 (2025-04-15)
-------------------

2.13.0 (2025-02-15)
-------------------
* fix: pointcloud_octomap_updater not cleaning objects at max_range (`#3294 <https://github.com/ros-planning/moveit2/issues/3294>`_)
* fix: OctoMap and Filtered_Cloud Not Updating During Movement Execution (`#3209 <https://github.com/ros-planning/moveit2/issues/3209>`_)
* Update deprecated tf2 imports from .h to .hpp (`#3197 <https://github.com/ros-planning/moveit2/issues/3197>`_)
* Contributors: Marco Magri, Sebastian Castro

2.12.0 (2024-11-29)
-------------------
* Enhancement/use hpp for headers (`#3113 <https://github.com/ros-planning/moveit2/issues/3113>`_)
* Contributors: Tom Noble

2.11.0 (2024-09-16)
-------------------
* Replace obsolete header (`#2978 <https://github.com/moveit/moveit2/issues/2978>`_)
* Fixed segmentation fault in depth_image_octomap_updater (`#2963 <https://github.com/moveit/moveit2/issues/2963>`_)
* Fix deprecation warning (`#2922 <https://github.com/moveit/moveit2/issues/2922>`_)
* Contributors: CihatAltiparmak, Robert Haschke, Sebastian Jahr

2.10.0 (2024-06-13)
-------------------
* Fix segmentation fault in mesh_filter/gl_renderer (`#2834 <https://github.com/moveit/moveit2/issues/2834>`_)
* Migrate ros-planning org to moveit (`#2847 <https://github.com/moveit/moveit2/issues/2847>`_)
  * Rename github.com/ros-planning -> github.com/moveit
  * Rename ros-planning.github.io -> moveit.github.io
  * Rename ros-planning organization in docker and CI workflow files
  - ghcr.io/ros-planning -> ghcr.io/moveit
  - github.repository == 'moveit/*''
* Unify log names (`#2720 <https://github.com/moveit/moveit2/issues/2720>`_)
  Co-authored-by: Abishalini Sivaraman <abi.gpuram@gmail.com>
* CMake format and lint in pre-commit (`#2683 <https://github.com/moveit/moveit2/issues/2683>`_)
* Contributors: CihatAltiparmak, Robert Haschke, Sebastian Jahr, Tyler Weaver

2.9.0 (2024-01-09)
------------------
* (moveit_ros) add missing CYLINDER check (`#2640 <https://github.com/ros-planning/moveit2/issues/2640>`_)
  As this check was missing, the CYLINDER check later on was unreachable
* Node logging in moveit_core (`#2503 <https://github.com/ros-planning/moveit2/issues/2503>`_)
* Use node logging in moveit_ros (`#2482 <https://github.com/ros-planning/moveit2/issues/2482>`_)
* Add new clang-tidy style rules (`#2177 <https://github.com/ros-planning/moveit2/issues/2177>`_)
* Update pre-commit and add to .codespell_words (`#2465 <https://github.com/ros-planning/moveit2/issues/2465>`_)
* Merge branch 'main' into dependabot/github_actions/SonarSource/sonarcloud-github-c-cpp-2
* Update clang-format-14 with QualifierAlignment (`#2362 <https://github.com/ros-planning/moveit2/issues/2362>`_)
  * Set qualifier order in .clang-format
  * Ran pre-commit to update according to new style guide
* Converts float to double (`#2343 <https://github.com/ros-planning/moveit2/issues/2343>`_)
  * Limiting the scope of variables `#874 <https://github.com/ros-planning/moveit2/issues/874>`_
  Limited the scope of variables in moveit_core/collision_detection
  * Update moveit_core/collision_detection/src/collision_octomap_filter.cpp
  Co-authored-by: AndyZe <andyz@utexas.edu>
  * Update moveit_core/collision_detection/src/collision_octomap_filter.cpp
  Co-authored-by: AndyZe <andyz@utexas.edu>
  * Update moveit_core/collision_detection/src/collision_octomap_filter.cpp
  Co-authored-by: AndyZe <andyz@utexas.edu>
  * convert float to double
  * change double to float
  * Feedback fixes
  * Introduced variables removed from previous merge commit
  * Updated GL_Renderer function definitions with double instead of float
  * Changed update() function arguments to float since it is a derived virtual function and needs to be overriden
  * Fixed all override errors in visualization
  * *Fixed override errors in perception
  *Changed reinterpret_cast to double* from float*
  * change variable types to fit function definition
  * Fixed clang-tidy warnings
  * Fixed scope of reusable variables
  ---------
  Co-authored-by: Salah Soliman <salahsoliman96@gmail.com>
  Co-authored-by: AndyZe <andyz@utexas.edu>
  Co-authored-by: Henning Kayser <henningkayser@picknik.ai>
* Merge branch 'main' into dependabot/github_actions/SonarSource/sonarcloud-github-c-cpp-2
* Contributors: Marq Rasmussen, Matthijs van der Burgh, Sebastian Jahr, Shobuj Paul, Tyler Weaver

2.8.0 (2023-09-10)
------------------
* Replaced numbers with SystemDefaultsQos() (`#2271 <https://github.com/ros-planning/moveit2/issues/2271>`_)
* Use `isnan` in `DepthImageOctomapUpdater` (`#2201 <https://github.com/ros-planning/moveit2/issues/2201>`_)
* Contributors: Ezra Brooks, Shobuj Paul

2.7.4 (2023-05-18)
------------------

2.7.3 (2023-04-24)
------------------
* Replace check for the ROS_DISTRO env variable with a check for the rclcpp version (`#2135 <https://github.com/ros-planning/moveit2/issues/2135>`_)
* Replace Variable PROJECT_NAME in CMakeLists.txt with the actual name (`#2020 <https://github.com/ros-planning/moveit2/issues/2020>`_)
* Contributors: Jafar, Shobuj Paul

2.7.2 (2023-04-18)
------------------
* Switch from qos_event.hpp to event_handler.hpp (`#2111 <https://github.com/ros-planning/moveit2/issues/2111>`_)
  * Switch from qos_event.hpp to event_handler.hpp
  * moveit_common: Add a cmake interface library to keep humble support on main
  * Include qos_event.hpp or event_handler.hpp depending on the ROS 2 version
  * Fix ament_lint_cmake
  * Fix clang-tidy
  * PRIVATE linking in some cases
  * Update moveit_common/cmake/moveit_package.cmake
  Co-authored-by: Chris Thrasher <chrisjthrasher@gmail.com>
  * Fix servo and cleanup excessive CMake variable usage
  * Cleanup & make compiling
  * Small variable naming and const cleanup
  * Restore OpenCV linking
  * Public/private linking fixup
  * Revert "Restore OpenCV linking"
  This reverts commit 57a9efa806e59223e35a1f7e998d7b52f930c263.
  ---------
  Co-authored-by: JafarAbdi <jafar.uruc@gmail.com>
  Co-authored-by: Jafar <cafer.abdi@gmail.com>
  Co-authored-by: AndyZe <andyz@utexas.edu>
  Co-authored-by: Chris Thrasher <chrisjthrasher@gmail.com>
* Update pre-commit (`#2094 <https://github.com/ros-planning/moveit2/issues/2094>`_)
* Contributors: Sebastian Jahr, Shobuj Paul

2.7.1 (2023-03-23)
------------------
* Fix member naming (`#1949 <https://github.com/ros-planning/moveit2/issues/1949>`_)
  * Update clang-tidy rules for readability-identifier-naming
  Co-authored-by: Sebastian Jahr <sebastian.jahr@picknik.ai>
* Contributors: Robert Haschke

2.7.0 (2023-01-29)
------------------
* converted characters from string format to character format (`#1881 <https://github.com/ros-planning/moveit2/issues/1881>`_)
* Fix BSD license in package.xml (`#1796 <https://github.com/ros-planning/moveit2/issues/1796>`_)
  * fix BSD license in package.xml
  * this must also be spdx compliant
* Enable `-Wold-style-cast` (`#1770 <https://github.com/ros-planning/moveit2/issues/1770>`_)
* Use sensor data QOS profile for sensor_msgs::Image and sensor_msgs::PointCloud (`#664 <https://github.com/ros-planning/moveit2/issues/664>`_)
  Co-authored-by: Henry Moore <henrygerardmoore@gmail.com>
  Co-authored-by: Tyler Weaver <tyler@picknik.ai>
* Remove `MOVEIT_LIB_NAME` (`#1751 <https://github.com/ros-planning/moveit2/issues/1751>`_)
  It's more readable and searchable if we just spell out the target
  name.
* Add braces around blocks. (`#999 <https://github.com/ros-planning/moveit2/issues/999>`_)
* Use <> for non-local headers (`#1734 <https://github.com/ros-planning/moveit2/issues/1734>`_)
  Unless a header lives in the same or a child directory of the file
  including it, it's recommended to use <> for the #include statement.
  For more information, see the C++ Core Guidelines item SF.12
  https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#sf12-prefer-the-quoted-form-of-include-for-files-relative-to-the-including-file-and-the-angle-bracket-form-everywhere-else
* Used C++ style cast instead of C style cast  (`#1628 <https://github.com/ros-planning/moveit2/issues/1628>`_)
  Co-authored-by: Henning Kayser <henningkayser@picknik.ai>
* Fix clang-tidy issues (`#1706 <https://github.com/ros-planning/moveit2/issues/1706>`_)
  * Blindly apply automatic clang-tidy fixes
  * Exemplarily cleanup a few automatic clang-tidy fixes
  * Clang-tidy fixups
  * Missed const-ref fixups
  * Fix unsupported non-const -> const
  * More fixes
  Co-authored-by: Henning Kayser <henningkayser@picknik.ai>
* Contributors: Abhijeet Das Gupta, Chris Thrasher, Christian Henkel, Cory Crean, Nathan Brooks, Robert Haschke, Sameer Gupta

2.6.0 (2022-11-10)
------------------
* Merge PR `#1553 <https://github.com/ros-planning/moveit2/issues/1553>`_: Improve cmake files
* Use standard exported targets: export\_${PROJECT_NAME} -> ${PROJECT_NAME}Targets
* Improve CMake usage (`#1550 <https://github.com/ros-planning/moveit2/issues/1550>`_)
* Remove __has_include statements (`#1481 <https://github.com/ros-planning/moveit2/issues/1481>`_)
* Contributors: Robert Haschke, Sebastian Jahr, Vatan Aksoy Tezer

2.5.3 (2022-07-28)
------------------
* pointcloud_octomap_updater: Don't return false when not finding optional parameter (`#1418 <https://github.com/ros-planning/moveit2/issues/1418>`_)
  * Don't return false when not finding optional parameter
  * Update moveit_ros/perception/pointcloud_octomap_updater/src/pointcloud_octomap_updater.cpp
  Co-authored-by: AndyZe <andyz@utexas.edu>
  Co-authored-by: AndyZe <andyz@utexas.edu>
  Co-authored-by: Vatan Aksoy Tezer <vatan@picknik.ai>
* Contributors: Jafar

2.5.2 (2022-07-18)
------------------
* Remove no longer needed no-pedantic option in moveit_ros_occupancy_map_monitor package (`#1397 <https://github.com/ros-planning/moveit2/issues/1397>`_)
* Merge remote-tracking branch 'origin/main' into feature/msa
* Removing more boost usage (`#1372 <https://github.com/ros-planning/moveit2/issues/1372>`_)
* Merge remote-tracking branch 'upstream/main' into feature/msa
* Removing some boost usage (`#1331 <https://github.com/ros-planning/moveit2/issues/1331>`_)
  Co-authored-by: Vatan Aksoy Tezer <vatan@picknik.ai>
* Remove unnecessary rclcpp.hpp includes (`#1333 <https://github.com/ros-planning/moveit2/issues/1333>`_)
* Update plugin library paths (`#1304 <https://github.com/ros-planning/moveit2/issues/1304>`_)
* Merge pull request `#3106 <https://github.com/ros-planning/moveit2/issues/3106>`_ from v4hn/pr-master-bind-them-all / banish bind()
* Fix clang-tidy
* banish bind()
* various: prefer objects and references over pointers
* Contributors: David V. Lu, Henry Moore, Jafar, Michael Görner, Nathan Brooks, Robert Haschke, Sebastian Jahr, Vatan Aksoy Tezer, v4hn

2.5.1 (2022-05-31)
------------------

2.5.0 (2022-05-26)
------------------
* Enable cppcheck (`#1224 <https://github.com/ros-planning/moveit2/issues/1224>`_)
  Co-authored-by: jeoseo <jeongwooseo2012@gmail.com>
* Make moveit_common a 'depend' rather than 'build_depend' (`#1226 <https://github.com/ros-planning/moveit2/issues/1226>`_)
* Remove unused includes for boost::bind (`#1220 <https://github.com/ros-planning/moveit2/issues/1220>`_)
* Avoid bind(), use lambdas instead (`#1204 <https://github.com/ros-planning/moveit2/issues/1204>`_)
  Adaption of https://github.com/ros-planning/moveit/pull/3106
* banish bind()
  source:https://github.com/ros-planning/moveit/pull/3106/commits/a2911c80c28958c1fce8fb52333d770248c4ec05; required minor updates compared to original source commit in order to ensure compatibility with ROS2
* various: prefer object and references over pointers
  source: https://github.com/ros-planning/moveit/pull/3106/commits/1a8e5715e3142a92977ac585031b9dc1871f8718; this commit contains minor changes when compared to the source commit which it is based on, these changes are limited to ensuring compatibility with ROS2.
* Remove new operators (`#1135 <https://github.com/ros-planning/moveit2/issues/1135>`_)
  replace new operator with make_shared
* Merge https://github.com/ros-planning/moveit/commit/ab42a1d7017b27eb6c353fb29331b2da08ab0039
* 1.1.9
* Use GLEW::GLEW link target (`#3079 <https://github.com/ros-planning/moveit2/issues/3079>`_)
  While ${GLEW_LIBRARIES} works on Ubuntu, it fails on newer installs of GLEW.
* Misc fixes for time and transforms (`#768 <https://github.com/ros-planning/moveit2/issues/768>`_)
  * Fix setting shape_transform_cache_lookup_wait_time from seconds
  * Fix setting last_update_time from seconds
  * Check the return value of canTransform
* Fix use of std::bind (`#3048 <https://github.com/ros-planning/moveit2/issues/3048>`_)
  Fixup for ab42a1d7017b27eb6c353fb29331b2da08ab0039 (`#2967 <https://github.com/ros-planning/moveit2/issues/2967>`_)
* 1.1.8
* 1.1.7
* Switch to std::bind (`#2967 <https://github.com/ros-planning/moveit2/issues/2967>`_)
  * boost::bind -> std::bind
  grep -rlI --exclude-dir=.git "boost::bind" | xargs sed -i 's/boost::bind/std::bind/g'
  * Convert bind placeholders
  grep -rlI --exclude-dir=.git " _[0-9]" | xargs sed -i 's/ _\([0-9]\)/ std::placeholders::_\1/g'
  * Update bind include header
  grep -rlI --exclude-dir=.git "boost/bind" | xargs sed -i 's#boost/bind.hpp#functional#'
* Add ns for depth image & pointcloud octomap updaters (`#2916 <https://github.com/ros-planning/moveit2/issues/2916>`_)
* 1.1.6
* Contributors: Abishalini, Henning Kayser, Jafar, Jafar Abdi, Jochen Sprickerhof, Michael Görner, Robert Haschke, Sencer Yazıcı, Stephanie Eng, Tim Redick, Tobias Fischer, jeoseo, v4hn

2.4.0 (2022-01-20)
------------------
* Fix boost linking errors for Windows (`#957 <https://github.com/ros-planning/moveit2/issues/957>`_)
* moveit_build_options()
  Declare common build options like CMAKE_CXX_STANDARD, CMAKE_BUILD_TYPE,
  and compiler options (namely warning flags) once.
  Each package depending on moveit_core can use these via moveit_build_options().
* Contributors: Akash, Robert Haschke

2.3.2 (2021-12-29)
------------------

2.3.1 (2021-12-23)
------------------
* Replaced C-Style Cast with C++ Style Cast. (`#935 <https://github.com/ros-planning/moveit2/issues/935>`_)
* Add codespell to precommit, fix A LOT of spelling mistakes (`#934 <https://github.com/ros-planning/moveit2/issues/934>`_)
* Enforce package.xml format 3 Schema (`#779 <https://github.com/ros-planning/moveit2/issues/779>`_)
* Update Maintainers of MoveIt package (`#697 <https://github.com/ros-planning/moveit2/issues/697>`_)
* clipped points should only be considered up to the max_range (`#2848 <https://github.com/ros-planning/moveit/issues/2848>`_)
* clang-tidy: modernize-make-shared, modernize-make-unique (`#2762 <https://github.com/ros-planning/moveit/issues/2762>`_)
* Contributors: Dave Coleman, David V. Lu!!, Henning Kayser, Kaustubh, Michael Görner, Robert Haschke, pvanlaar

2.3.0 (2021-10-08)
------------------
* Fix warnings in Galactic and Rolling (`#598 <https://github.com/ros-planning/moveit2/issues/598>`_)
  * Use __has_includes preprocessor directive for deprecated headers
  * Fix parameter template types
  * Proper initialization of smart pointers, rclcpp::Duration
* Fixes for Windows (`#530 <https://github.com/ros-planning/moveit2/issues/530>`_)
* Refactors for OccMapTree in PlanningScene (`#2684 <https://github.com/ros-planning/moveit2/issues/2684>`_)
* Move OccMapTree to moveit_core/collision_detection
* Contributors: Akash, Henning Kayser, Simon Schmeisser, Tyler Weaver, Vatan Aksoy Tezer, Nisala Kalupahana, Jorge Nicho, Tyler Weaver, Lior Lustgarten

2.2.1 (2021-07-12)
------------------

2.2.0 (2021-06-30)
------------------
* Compilation fixes for MoveIt on macOS (`#498 <https://github.com/ros-planning/moveit2/issues/498>`_)
* [sync] MoveIt's master branch up-to https://github.com/ros-planning/moveit/commit/0d0a6a171b3fbea97a0c4f284e13433ba66a4ea4
  * document solution in ROS_ERROR on failed self-filtering (`#2627 <https://github.com/ros-planning/moveit/issues/2627>`_)
  * Fixed flood of errors on startup for `mesh_filter` (`#2550 <https://github.com/ros-planning/moveit/issues/2550>`_)
  * Enable mesh filter (`#2448 <https://github.com/ros-planning/moveit/issues/2448>`_)
* Contributors: Jafar Abdi, JafarAbdi, John Stechschulte, Michael Görner, Nisala Kalupahana, Robert Haschke, Simon Schmeisser, Tyler Weaver

2.1.4 (2021-05-31)
------------------

2.1.3 (2021-05-22)
------------------

2.1.2 (2021-04-20)
------------------

2.1.1 (2021-04-12)
------------------
* Fix porting errors in depth_image_octomap_updater (`#383 <https://github.com/ros-planning/moveit2/issues/383>`_)
  * Fix error of not being able to receive depth image
  * Fix mismatching time source
* Port moveit_ros_perception/depth_image_octomap_updater (`#354 <https://github.com/ros-planning/moveit2/issues/354>`_)
* Fix EXPORT install in CMake (`#372 <https://github.com/ros-planning/moveit2/issues/372>`_)
* [fix] export cmake library install (`#339 <https://github.com/ros-planning/moveit2/issues/339>`_)
* Porting moveit_ros_perception/pointcloud_octomap_updater (`#307 <https://github.com/ros-planning/moveit2/issues/307>`_)
* Fix repo URLs in package.xml files
* Contributors: Henning Kayser, Tyler Weaver, Yu Yan

2.0.0 (2020-10-13)
------------------

1.1.1 (2020-10-13)
------------------
* [fix] various issues with Noetic build (`#2327 <https://github.com/ros-planning/moveit/issues/2327>`_)
* [maint] Cleanup MSA includes (`#2351 <https://github.com/ros-planning/moveit/issues/2351>`_)
* [maint] Add comment to MOVEIT_CLASS_FORWARD (`#2315 <https://github.com/ros-planning/moveit/issues/2315>`_)
* Contributors: Felix von Drigalski, G.A. vd. Hoorn, Robert Haschke

1.1.0 (2020-09-04)
------------------
* [feature] Utilize new geometric_shapes functions to improve performance (`#2038 <https://github.com/ros-planning/moveit/issues/2038>`_)
* [fix] Various fixes for upcoming Noetic release (`#2180 <https://github.com/ros-planning/moveit/issues/2180>`_)
* [fix] Fix getTransform() (`#2113 <https://github.com/ros-planning/moveit/issues/2113>`_)
* [fix] depth_image_octomap_updater: correctly set properties of debug images (`#1653 <https://github.com/ros-planning/moveit/issues/1653>`_)
* [maint] Optional cpp version setting (`#2166 <https://github.com/ros-planning/moveit/issues/2166>`_)
* [maint] clang-tidy fixes (`#2050 <https://github.com/ros-planning/moveit/issues/2050>`_, `#2004 <https://github.com/ros-planning/moveit/issues/2004>`_, `#1419 <https://github.com/ros-planning/moveit/issues/1419>`_)
* [maint] Fix errors: catkin_lint 1.6.7 (`#1987 <https://github.com/ros-planning/moveit/issues/1987>`_)
* [maint] Replace namespaces robot_state and robot_model with moveit::core (`#1924 <https://github.com/ros-planning/moveit/issues/1924>`_)
* [maint] NAMED logging for moveit_ros_perception (`#1897 <https://github.com/ros-planning/moveit/issues/1897>`_)
* [maint] Fix various build issues on Windows (`#1880 <https://github.com/ros-planning/moveit/issues/1880>`_)
* [maint] Fix compiler warnings (`#1773 <https://github.com/ros-planning/moveit/issues/1773>`_)
* [maint] Switch from include guards to pragma once (`#1615 <https://github.com/ros-planning/moveit/issues/1615>`_)
* [maint] Remove ! from MoveIt name (`#1590 <https://github.com/ros-planning/moveit/issues/1590>`_)
* Contributors: Ayush Garg, Bjar Ne, Dale Koenig, Dave Coleman, Henning Kayser, Jonathan Binney, Mahmoud Ahmed Selim, Markus Vieth, Martin Pecka, Matthias Nieuwenhuisen, Michael Görner, Robert Haschke, Sean Yen, Tyler Weaver, Yu, Yan, jschleicher

1.0.6 (2020-08-19)
------------------
* [maint] Migrate to clang-format-10
* [maint] Optimize includes (`#2229 <https://github.com/ros-planning/moveit/issues/2229>`_)
* [maint] Further increase acceptance threshold for mesh-filter test
* [maint] Prefer vendor-specific OpenGL library
* Contributors: Markus Vieth, Robert Haschke

1.0.5 (2020-07-08)
------------------
* [maint] Fix mesh_filter test (`#2044 <https://github.com/ros-planning/moveit/issues/2044>`_)
* Contributors: Bjar Ne

1.0.4 (2020-05-30)
------------------

1.0.3 (2020-04-26)
------------------
* [maint] Apply clang-tidy fix to entire code base (`#1394 <https://github.com/ros-planning/moveit/issues/1394>`_)
* [maint] Fix errors: catkin_lint 1.6.7 (`#1987 <https://github.com/ros-planning/moveit/issues/1987>`_)
* [maint] Windows build fixes
  * Fix header inclusion and other MSVC build errors (`#1636 <https://github.com/ros-planning/moveit/issues/1636>`_)
  * Fix binary artifact install locations. (`#1575 <https://github.com/ros-planning/moveit/issues/1575>`_)
* [maint] Use CMAKE_CXX_STANDARD to enforce c++14 (`#1607 <https://github.com/ros-planning/moveit/issues/1607>`_)
* [maint] Allow subclassing of point_containment_filter::ShapeMask. (`#1457 <https://github.com/ros-planning/moveit/issues/1457>`_)
* [fix]   `depth_image_octomap_updater`: reset depth transfer function to standard values (`#1661 <https://github.com/ros-planning/moveit/issues/1661>`_)
* [fix]   `depth_image_octomap_updater`: correctly set properties of debug images (`#1652 <https://github.com/ros-planning/moveit/issues/1652>`_)
* [maint] Move `occupancy_map_monitor` into its own package (`#1533 <https://github.com/ros-planning/moveit/issues/1533>`_)
* Contributors: Martin Pecka, Matthias Nieuwenhuisen, Robert Haschke, Sean Yen, Yu, Yan, jschleicher

1.0.2 (2019-06-28)
------------------
* [maintenance] Removed unnecessary null pointer checks on deletion (`#1410 <https://github.com/ros-planning/moveit/issues/1410>`_)
* Contributors: Mahmoud Ahmed Selim

1.0.1 (2019-03-08)
------------------
* [improve] Apply clang tidy fix to entire code base (Part 1) (`#1366 <https://github.com/ros-planning/moveit/issues/1366>`_)
* Contributors: Yu, Yan

1.0.0 (2019-02-24)
------------------
* [fix] catkin_lint issues (`#1341 <https://github.com/ros-planning/moveit/issues/1341>`_)
* Contributors: Robert Haschke

0.10.8 (2018-12-24)
-------------------

0.10.7 (2018-12-13)
-------------------

0.10.6 (2018-12-09)
-------------------
* [maintenance] Use createUniqueInstance() (`#1104 <https://github.com/ros-planning/moveit/issues/1104>`_)
* [maintenance] Enforce OpenMP support for perception (`#1234 <https://github.com/ros-planning/moveit/issues/1234>`_)
* [maintenance] Replaced Eigen::Affine3d -> Eigen::Isometry3d (`#1096 <https://github.com/ros-planning/moveit/issues/1096>`_)
* [maintenance] Use C++14 (`#1146 <https://github.com/ros-planning/moveit/issues/1146>`_)
* Contributors: Alex Moriarty, Michael Görner, Robert Haschke

0.10.5 (2018-11-01)
-------------------

0.10.4 (2018-10-29)
-------------------

0.10.3 (2018-10-29)
-------------------
* [fix] compiler warnings (`#1089 <https://github.com/ros-planning/moveit/issues/1089>`_)
* Contributors: Robert Haschke

0.10.2 (2018-10-24)
-------------------
* [fix] Eigen alignment issuses due to missing aligned allocation (`#1039 <https://github.com/ros-planning/moveit/issues/1039>`_)
* [fix] DepthImageOctomapUpdater not found error (`#954 <https://github.com/ros-planning/moveit/issues/954>`_)
* [fix] planning scene lock when octomap updates too quickly (`#920 <https://github.com/ros-planning/moveit/issues/920>`_)
* [enhancement] error message in shape_mask (`#828 <https://github.com/ros-planning/moveit/issues/828>`_)
* [maintenance] various compiler warnings (`#1038 <https://github.com/ros-planning/moveit/issues/1038>`_)
* [maintenance] disable unittests for moveit_ros_perception ... due to broken Mesa OpenGL (since version 17.x?) (`#982 <https://github.com/ros-planning/moveit/issues/982>`_)
* [maintenance] add minimum required pluginlib version (`#927 <https://github.com/ros-planning/moveit/issues/927>`_)
* Contributors: Adrian Zwiener, Martin Günther, Michael Görner, Mikael Arguedas, Mohmmad Ayman, Ridhwan Luthra, Robert Haschke, mike lautman

0.10.1 (2018-05-25)
-------------------
* boost::shared_ptr -> std::shared_ptr
* migration from tf to tf2 API (`#830 <https://github.com/ros-planning/moveit/issues/830>`_)
* [fix] make OpenGL parts optional (`#698 <https://github.com/ros-planning/moveit/issues/698>`_)
* Contributors: Bence Magyar, Ian McMahon, Lukas Bulwahn, Michael Görner, Mikael Arguedas, Robert Haschke

0.9.11 (2017-12-25)
-------------------

0.9.10 (2017-12-09)
-------------------
* [improve] removed deprecated pluginlib macro (`#677 <https://github.com/ros-planning/moveit/issues/677>`_)
* Contributors: Mikael Arguedas

0.9.9 (2017-08-06)
------------------

0.9.8 (2017-06-21)
------------------

0.9.7 (2017-06-05)
------------------

0.9.6 (2017-04-12)
------------------
* [fix][moveit_ros_robot_interaction] `catkin_make -DCMAKE_ENABLE_TESTING=0` failure (`#478 <https://github.com/ros-planning/moveit/issues/478>`_)
* Contributors: Michael Goerner

0.9.5 (2017-03-08)
------------------
* [fix][moveit_ros_warehouse] gcc6 build error `#423 <https://github.com/ros-planning/moveit/pull/423>`_
* [enhancement] Remove "catch (...)" instances, catch std::exception instead of std::runtime_error (`#445 <https://github.com/ros-planning/moveit/issues/445>`_)
* Contributors: Bence Magyar, Dave Coleman

0.9.4 (2017-02-06)
------------------
* [maintenance] Remove custom cmake modules (`#418 <https://github.com/ros-planning/moveit/issues/418>`_)
* [maintenance] clang-format upgraded to 3.8 (`#367 <https://github.com/ros-planning/moveit/issues/367>`_)
* Contributors: Dave Coleman, Jochen Sprickerhof

0.9.3 (2016-11-16)
------------------

0.9.2 (2016-11-05)
------------------
* [Maintenace] Auto format codebase using clang-format (`#284 <https://github.com/ros-planning/moveit/issues/284>`_)
* Contributors: Dave Coleman

0.6.6 (2016-06-08)
------------------
* replaced cmake_modules dependency with eigen
* [jade] eigen3 adjustment
* remove unknown dependency sensor_msgs_generate_cpp
  dependencies are pulled in via ${catkin_LIBRARIES}
* Find X11 for build on OS X 10.11
* set empty display function for glut window
  With freeglut 3.0 moveit aborts over here, printing
  > ERROR: No display callback registered for window 1
  According to https://sourceforge.net/p/freeglut/bugs/229/
  and https://www.opengl.org/resources/libraries/glut/spec3/node46.html
  a callback *must* be registered for each window.
  With this patch moveit starts up as expected.
* Remove OpenMP parallelization, fixes `#563 <https://github.com/ros-planning/moveit_ros/issues/563>`_
* Removed trailing whitespace from entire repository
* last comment
* Added missing dependency on moveit_msgs package
* Contributors: Andriy Petlovanyy, Dave Coleman, Isaac I.Y. Saito, Kentaro Wada, Robert Haschke, Stefan Kohlbrecher, dg, v4hn

0.6.5 (2015-01-24)
------------------
* update maintainers
* adding RAII-based locking for OccMapTree
* moving lazy_free_space_updater into it's own library
* Contributors: Jonathan Bohren, Michael Ferguson

0.6.4 (2014-12-20)
------------------

0.6.3 (2014-12-03)
------------------
* port `moveit_ros#445 <https://github.com/ros-planning/moveit_ros/issues/445>`_ to indigo
* disable test that needs display when no display defined
* GL_TYPE() is a function in newer versions of OpenGL, this fixes tests on Ubuntu 14.04
* Contributors: Michael Ferguson

0.6.2 (2014-10-31)
------------------

0.6.1 (2014-10-31)
------------------
* fix linking error on OSX
* Contributors: Michael Ferguson

0.6.0 (2014-10-27)
------------------
* Fixing invalid iterators if filtered_cloud_topic is not set.
  Adding missing dependency on sensor_msgs.
  Fixing indentation, whitespace, and tabs.
  Incrementing PointCloud2Iterator pixel-at-a-time, not byte-at-a-time.
* remove PCL dependency
* Fixed issue with unordered_map and libc++ (LLVM, Mac OS X Mavericks)
  libc++ doesn't have std::tr1::unordered_map, just std::unordered_map
* Fixing OpenGL gl.h and glu.h inclusion on Mac OS X
* Contributors: Jason Ziglar, Marco Esposito, Sachin Chitta, Vincent Rabaud

0.5.19 (2014-06-23)
-------------------
* Fix [-Wreorder] warning.
* Address [cppcheck: duplicateExpression] error.
  The existing check for NaNs is in fact correct for IEEE-compliant floating
  numbers, i.e., if (a == a) then a is not a NaN, but confuses static code
  analyzers. This fix instead uses the isnan(a) macro from <cmath>.
* Prevent future conflicts between STL and Boost.
  mesh_filter_base.cpp was doing:
  using namespace std;
  using namespace boost;
  Considering that Boost is a testing ground for future standard additions,
  bringing the two namespaces into scope in the same translation unit is not
  the best idea. In this particular file, there's a potential conflict between
  C++'s and Boost's shared_ptr implementation.
* Make creation of std::pairs future-compiler-proof.
  Details:
  http://stackoverflow.com/questions/14623958/breaking-change-in-c11-with-make-pair-ty1-val1-const-ty2-val2
* Contributors: Adolfo Rodriguez Tsouroukdissian

0.5.18 (2014-03-23)
-------------------

0.5.17 (2014-03-22)
-------------------
* update build system for ROS indigo
* update maintainer e-mail
* Contributors: Ioan Sucan

0.5.16 (2014-02-27)
-------------------

0.5.14 (2014-02-06)
-------------------

0.5.13 (2014-02-06)
-------------------

0.5.12 (2014-01-03)
-------------------

0.5.11 (2014-01-03)
-------------------

0.5.10 (2013-12-08)
-------------------
* comply to the new Table.msg
* Contributors: Vincent Rabaud

0.5.9 (2013-12-03)
------------------
* fix cloud offset

0.5.8 (2013-10-11)
------------------
* adds compliance for mesa versions <9.2

0.5.7 (2013-10-01)
------------------

0.5.6 (2013-09-26)
------------------
* fix `#320 <https://github.com/ros-planning/moveit_ros/issues/320>`_.
* fix `#318 <https://github.com/ros-planning/moveit_ros/issues/318>`_.

0.5.5 (2013-09-23)
------------------
* remove dep on pcl (pcl_conversions is sufficient)

0.5.4 (2013-08-14)
------------------
* add dependency on OpenCV2
* Pointcloud_octomap_updater compilation flags fixed

0.5.2 (2013-07-15)
------------------

0.5.1 (2013-07-14)
------------------
* find PCL separately

0.5.0 (2013-07-12)
------------------
* use pcl_conversions instead of pcl_ros
* white space fixes (tabs are now spaces)

0.4.5 (2013-07-03)
------------------

0.4.4 (2013-06-26)
------------------
* Fixes linkedit error on OS X
