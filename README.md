# Checkouts bug
Failure with profiles.clj

        lein run -m compojure.checkouts 
        Exception in thread "main" java.lang.ClassNotFoundException: compojure.checkouts
        	at java.net.URLClassLoader$1.run(URLClassLoader.java:202)
        	at java.security.AccessController.doPrivileged(Native Method)
        	at java.net.URLClassLoader.findClass(URLClassLoader.java:190)
        	at clojure.lang.DynamicClassLoader.findClass(DynamicClassLoader.java:61)
        	at java.lang.ClassLoader.loadClass(ClassLoader.java:306)
        	at java.lang.ClassLoader.loadClass(ClassLoader.java:247)
        	at java.lang.Class.forName0(Native Method)
        	at java.lang.Class.forName(Class.java:249)
        	at clojure.lang.RT.classForName(RT.java:2039)
        	at clojure.lang.Reflector.invokeStaticMethod(Reflector.java:199)
        	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:39)
        	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:25)
        	at java.lang.reflect.Method.invoke(Method.java:597)
        	at clojure.lang.Reflector.invokeMatchingMethod(Reflector.java:93)
        	at clojure.lang.Reflector.invokeStaticMethod(Reflector.java:207)
        	at user$eval5.invoke(NO_SOURCE_FILE:1)
        	at clojure.lang.Compiler.eval(Compiler.java:6511)
        	at clojure.lang.Compiler.eval(Compiler.java:6501)
        	at clojure.lang.Compiler.eval(Compiler.java:6477)
        	at clojure.core$eval.invoke(core.clj:2797)
        	at clojure.main$eval_opt.invoke(main.clj:297)
        	at clojure.main$initialize.invoke(main.clj:316)
        	at clojure.main$null_opt.invoke(main.clj:349)
        	at clojure.main$main.doInvoke(main.clj:427)
        	at clojure.lang.RestFn.invoke(RestFn.java:421)
        	at clojure.lang.Var.invoke(Var.java:419)
        	at clojure.lang.AFn.applyToHelper(AFn.java:163)
        	at clojure.lang.Var.applyTo(Var.java:532)
        	at clojure.main.main(main.java:37)
        	
remove profiles.clj
    
        rm profiles.clj
        lein run -m compojure.checkouts
        Whooot! Checkouts working