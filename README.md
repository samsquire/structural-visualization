# structural-visualization

This repository is the idea we can use coloured grids to represents trees and graphs compactly by adding rules to the reading of the grid.

These rules are as follows:

* we switch between horizontal and vertical rendering for efficient use of space
* children are listed from left to right or top to bottom
* If we want to enumerate children, we do that separately, below the main diagram

See this diagram, the grid at the top represents the tree. Notice the colour codings.

![assumedlinks](https://raw.githubusercontent.com/samsquire/structural-visualization/main/linksassumption.png)


An idea for a simple visualization of complicated structures

# btree find

This diagram represents the following code:

![btree](https://raw.githubusercontent.com/samsquire/structural-visualization/main/btree.png)

Circle represents a loop, a triangle represents an if statement.

```
 def find(self, key):
        leaf = self
        next_children = self.children
        last_child = self
        child = None
        parents = [self]
        found = False
        while found == False:
            next_children_changed = False
            for child in reversed(next_children):
                if key >= child.key:
                    # print("Inspecting {} <= {} ".format(child.key, key))
                    next_children = child.children
                    
                    last_child = leaf
                    parents.append(child)
                    leaf = child
                    next_children_changed = True
                    break
                    
                    
                        
                        
            if not next_children_changed:
                found = True

        return leaf, last_child, 
```

![complicated](https://raw.githubusercontent.com/samsquire/structural-visualization/main/complicated.png)

![threadstructure](https://raw.githubusercontent.com/samsquire/structural-visualization/main/graph.png)

![betterthreadstructure](https://raw.githubusercontent.com/samsquire/structural-visualization/main/graph2.png)

