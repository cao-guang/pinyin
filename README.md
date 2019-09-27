# pinyin
汉字转拼音，简单实用，不坑人


添加引用
```go
import(
"github.com/cao-guang/pinyin"
)
```
初始化调用
```go
func main()  {
   	pinyin.LoadingPYFileName("./data/pinyin.txt") //这里是字典文件路径程序启动调用一次，载入缓存
   	//demo
   	str1, err := pinyin.To_Py("汉字拼音", "", "") //默认造型： hanzipinyin
   	if err != nil {
   		fmt.Println(err)
   	}
   	fmt.Println(str1)
   	str2, err := pinyin.To_Py("汉字拼音", "", pinyin.Tone) //带声调：hànzìpīnyīn
   	if err != nil {
   		fmt.Println(err)
   	}
   	fmt.Println(str2)
   	str3, err := pinyin.To_Py("汉字拼音", "", pinyin.InitialsInCapitals) //首字母大写无声调：HanZiPinYin
   	if err != nil {
   		fmt.Println(err)
   	}
   	fmt.Println(str3)
   	str4, err := pinyin.To_Py("汉字拼音", "-", pinyin.InitialsInCapitals) //首字母大写无声调加-分割：Han-Zi-Pin-Yin
   	if err != nil {
   		fmt.Println(err)
   	}
   	fmt.Println(str4)
}
```
