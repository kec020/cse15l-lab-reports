This is the [link](https://github.com/kec020/markdown-parser) to my markdown-parse repository.

This is the [link](https://github.com/hahacen/markdown-parser) to the one I reviewed in week 7.


# Snippet 1

By looking at the VScode preview, ![snippet1](snippet1.png)
the expected output should be <code>[`google.com, google.com, ucsd.edu]</code>

This is my code in MarkdownParseTest.java for how I turned it into a test
![s1test](s1test.png)


The corresponding output when running the test:

For my implementation: Failed
![s1test-result](s1test-result.png)

For the implementation you reviewed in Week 7: Failed
![s1review-test-result](s1review-test-result.png)

I think there can be a small code change that will make my program work for snippet 1 and all related cases that use inline code with backticks. I need to first determine whether there is a <code>`</code>. If there exist the backticks, it shouold ignore the part between the backticks and update the starting index to find the brackets, parenthesis, and escaped brackets.



# Snippet 2
By looking at the VScode preview, ![snippet2](snippet2.png)
the expected output should be <code>[a.com, a.com(()), example.com]</code>

This is my code in MarkdownParseTest.java for how I turned it into a test
![s2test](s2test.png)


The corresponding output when running the test:

For my implementation: Failed
![s2test-result](s2test-result.png)

For the implementation you reviewed in Week 7: Failed
![s2review-test-result](s2review-test-result.png)

I think the code change may exceed 10 lines. Because I need to figure out when there is a `)` match after the `(` inside the , it should be the nested parentheses, brackets, and escaped brackets. The code for determining this situation might long.



# Snippet 3
By looking at the VScode preview, ![snippet3](snippet3.png)
the expected output should be <code>[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]</code>

This is my code in MarkdownParseTest.java for how I turned it into a test
![s3test](s3test.png)


The corresponding output when running the test:

For my implementation: Failed
![s3test-result](s3test-result.png)

For the implementation you reviewed in Week 7: Failed
![s3review-test-result](s3review-test-result.png)

For the last one, I think the code change can be small. I need to determine if there is newlines in brackets and parentheses. if yes, it needs to ignore the newlines, and update the index.