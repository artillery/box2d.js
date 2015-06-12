
project(box2d)

set(BOX2D_SRC Box2D_v2.2.1/Box2D)

add_library(box2d OBJECT
            ${BOX2D_SRC}/Collision/b2BroadPhase.cpp
            ${BOX2D_SRC}/Collision/b2CollideCircle.cpp
            ${BOX2D_SRC}/Collision/b2CollideEdge.cpp
            ${BOX2D_SRC}/Collision/b2CollidePolygon.cpp
            ${BOX2D_SRC}/Collision/b2Collision.cpp
            ${BOX2D_SRC}/Collision/b2Distance.cpp
            ${BOX2D_SRC}/Collision/b2DynamicTree.cpp
            ${BOX2D_SRC}/Collision/b2TimeOfImpact.cpp
            ${BOX2D_SRC}/Collision/Shapes/b2ChainShape.cpp
            ${BOX2D_SRC}/Collision/Shapes/b2CircleShape.cpp
            ${BOX2D_SRC}/Collision/Shapes/b2EdgeShape.cpp
            ${BOX2D_SRC}/Collision/Shapes/b2PolygonShape.cpp
            ${BOX2D_SRC}/Common/b2BlockAllocator.cpp
            ${BOX2D_SRC}/Common/b2Draw.cpp
            ${BOX2D_SRC}/Common/b2Math.cpp
            ${BOX2D_SRC}/Common/b2Settings.cpp
            ${BOX2D_SRC}/Common/b2StackAllocator.cpp
            ${BOX2D_SRC}/Common/b2Timer.cpp
            ${BOX2D_SRC}/Dynamics/b2Body.cpp
            ${BOX2D_SRC}/Dynamics/b2ContactManager.cpp
            ${BOX2D_SRC}/Dynamics/b2Fixture.cpp
            ${BOX2D_SRC}/Dynamics/b2Island.cpp
            ${BOX2D_SRC}/Dynamics/b2World.cpp
            ${BOX2D_SRC}/Dynamics/b2WorldCallbacks.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2ChainAndCircleContact.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2ChainAndPolygonContact.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2CircleContact.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2Contact.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2ContactSolver.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2EdgeAndCircleContact.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2EdgeAndPolygonContact.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2PolygonAndCircleContact.cpp
            ${BOX2D_SRC}/Dynamics/Contacts/b2PolygonContact.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2DistanceJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2FrictionJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2GearJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2Joint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2MouseJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2PrismaticJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2PulleyJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2RevoluteJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2RopeJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2WeldJoint.cpp
            ${BOX2D_SRC}/Dynamics/Joints/b2WheelJoint.cpp
            ${BOX2D_SRC}/Rope/b2Rope.cpp)

set(CMAKE_CXX_FLAGS "-std=c++11 -stdlib=libc++ -DATLAS -O3")
target_include_directories(box2d PUBLIC
  Box2D_v2.2.1
  ${COMMON_INCLUDE_PATHS}
)
