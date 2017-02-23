MatrixKit example that illustrates `use_frameworks!` error
----------------------------------------------------------

This trivial project demonstrates a compiler error when using MatrixKit with
`use_frameworks!` enabled. This is technically an Obj-C project, however the
same error would occur in a Swift project because the `use_frameworks!` setting
is required for Swift projects (Obj-C projects support both Frameworks and
Libraries. Swift projects **only** support Frameworks)

1. `pod install`
2. attempt to build the project
3. Success!
4. Uncomment `use_frameworks!` in the podfile
5. `pod install` again
6. Error: Unable to build module GHMarkdownParser.

(See https://github.com/matrix-org/matrix-ios-kit/issues/188)
