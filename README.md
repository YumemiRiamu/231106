# 231106</br>

비주얼프로그래밍 팀프로젝트 </br>

20191276 컴퓨터공학과 양용석</br>

1. MFC의 멀티쓰레드 구현</br>

코드


2. WinUI3 계산기 구현</br>

코드
```
//MainWindow.xaml
 <StackPanel Orientation="Vertical" HorizontalAlignment="Center" VerticalAlignment="Center">
     <TextBox x:Name="va"/>
     <TextBox x:Name="vb"/>
     <Button x:Name="myButton" Click="myButton_Click">+</Button>
     <Button x:Name="myButton1" Click="myButton_Click1">-</Button>
     <Button x:Name="myButton2" Click="myButton_Click2">*</Button>
     <Button x:Name="myButton3" Click="myButton_Click3">/</Button>
     <TextBox x:Name="vc"/>
 </StackPanel>
```

```
//MainWindow.xaml.cpp
 void MainWindow::myButton_Click(IInspectable const&, RoutedEventArgs const&) {
     double a, b, c;
     a = std::stod(va().Text().c_str());
     b = std::stod(vb().Text().c_str());
     c = a + b; vc().Text(std::to_wstring(c));
 }

 void MainWindow::myButton_Click1(IInspectable const&, RoutedEventArgs const&) {
     double a, b, c;
     a = std::stod(va().Text().c_str());
     b = std::stod(vb().Text().c_str());
     c = a - b; vc().Text(std::to_wstring(c));
 }

 void MainWindow::myButton_Click2(IInspectable const&, RoutedEventArgs const&) {
     double a, b, c;
     a = std::stod(va().Text().c_str());
     b = std::stod(vb().Text().c_str());
     c = a * b; vc().Text(std::to_wstring(c));
 }

 void MainWindow::myButton_Click3(IInspectable const&, RoutedEventArgs const&) {
     double a, b, c;
     a = std::stod(va().Text().c_str());
     b = std::stod(vb().Text().c_str());
     c = a / b; vc().Text(std::to_wstring(c));
 }
```

```
//MainWindow.xaml.h
 void myButton_Click(Windows::Foundation::IInspectable const& sender, Microsoft::UI::Xaml::RoutedEventArgs const& args);
 void myButton_Click1(Windows::Foundation::IInspectable const& sender, Microsoft::UI::Xaml::RoutedEventArgs const& args);
 void myButton_Click2(Windows::Foundation::IInspectable const& sender, Microsoft::UI::Xaml::RoutedEventArgs const& args);
 void myButton_Click3(Windows::Foundation::IInspectable const& sender, Microsoft::UI::Xaml::RoutedEventArgs const& args);
```
실행 화면

