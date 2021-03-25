# MP1_CS437
Part One:
To my knowledge the DominatorFinder classes method doAnalysis() was fully and correctly implemted in the code given to me. From this we can see all of the dominators for the statements in the GCD class. See output for more detailed breakdown on dominators for each statement. 

The only change made to the provided code was in line 17 of TestDominatorFinder.java the line String mainclass = "GCD"; was changed to String mainclass = "a1.GCD" becasue the package name is a1.

Part Two:
There are two lines in the TestSootCallGraph class that allow for each analysis method class hierarchy analysis (CHA) and  points-to analysis (PTA) to be run for the Example.java class. Commenting out the line enableCHACallGraph(); (line 48) and leaving enableSparkCallGraph(); will run the PTA while Commenting out the line enableSparkCallGraph(); (line 49) and leaving enableCHACallGraph(); will run the CHA. 

Looking at the output of both analyses it becomes evident that PTA is more precise, calling only 7 edges compared to the 12 edges called by CHA.

In terms of speed, for the example given there was not a drastic difference in runtime. The PTA took apporximately 8 seconds to run its analysis while the CHA took closer to 7 seconds to run.

Part Three:
1.Could not get the file described in the instructions to be generated.  

2.The code written for this section of part three gets all of the parameters for the logFieldAcc() method. For the Object o, the currentThread is used, for the name a toString() on the field reference is used, for isStatic the isStatic() is used, and for isWrite a try and catch is used with the DefBoxes() method which determines whether a read or write action is taken. 

If left most varible in te DefBoxes() list is of type soot.jimple.internal.JimpleLocal, it is a read action; If it is of type class soot.jimple.internal.JInstanceFieldRef or class soot.jimple.StaticFieldRef, it is a write action.

Output for this section:
Thread Thread-13 wrote static field <a1.HelloThread: int x>
Thread Thread-13 read instance field <a1.HelloThread$TestThread: int y> of object Thread[Thread-13,5,Soot Threadgroup]
Thread Thread-13 wrote instance field <a1.HelloThread$TestThread: int y> of object Thread[Thread-13,5,Soot Threadgroup]
Thread Thread-12 read instance field <a1.HelloThread$TestThread: int y> of object Thread[Thread-12,5,Soot Threadgroup]
Thread Thread-12 read static field <a1.HelloThread: int x>
Thread Thread-12 read static field <java.lang.System: java.io.PrintStream out>
