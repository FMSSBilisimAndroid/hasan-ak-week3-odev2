## GIF 1 


<img src ="https://github.com/FMSSBilisimAndroid/hasan-ak-week3-odev2/blob/master/gif_1.gif" width = 300 height = 500/>

## Araştırma Ödevi: Serializable ve Parcelabe Kavramları
**Serializable**

Serializable işaretlenebilir bir arayüzdür ya da boş interface olarak adlandırabiliriz. Önceden uygulanmış herhangi bir yöntemi yoktur.
Serializable, nesneyi bayt akışına dönüştürecek. Böylece kullanıcı bir aktivite arasındaki verileri başka bir aktiviteye aktarabilir.
Serializable'ın ana avantajı, veri oluşturma ve aktarmanın çok kolay olmasıdır, ancak parcelable ile karşılaştırıldığında yavaş bir süreçtir.

Aşağıda gösterildiği gibi basit bir serializable hale getirilebilir örneği

```
internal class serializableObject(var name: String) : Serializable
```


**Parcelable**

Parcelable, serializable'dan daha hızlıdır.Parcelable, nesneyi bayt akışına dönüştürecek ve verileri iki etkinlik arasında iletecek.
Parcelable kod yazmak, serializable'la kıyasla biraz karmaşıktır.Verileri iki aktivite arasında geçirirken daha fazla geçici nesne oluşturmaz.

Aşağıda gösterildiği gibi basit bir Parcelable örneği

``` 
import android.os.Parcel
import android.os.Parcelable
import android.os.Parcelable.Creator


internal class parcleObject : Parcelable {
    var name: String?

    protected constructor(`in`: Parcel) {
        name = `in`.readString()
    }

    constructor(name: String?) {
        this.name = name
    }

    override fun describeContents(): Int {
        return 0
    }

    override fun writeToParcel(dest: Parcel, flags: Int) {
        dest.writeString(name)
    }


    companion object {
        @JvmField
        val CREATOR: Creator<parcleObject?> = object : Creator<parcleObject?> {
            override fun createFromParcel(`in`: Parcel): parcleObject? {
                return parcleObject(`in`)
            }

            override fun newArray(size: Int): Array<parcleObject?> {
                return arrayOfNulls(size)
            }
        }
    }
}
```

## About Me

### Hi 👋, I'm Hasan

- 🔭 I’m currently working on Android
- 🌱 I’m currently learning Kotlin

## 📫 How to reach me:
  <a href="https://www.linkedin.com/in/hasanak">
    <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>
  
  ## :fire: My Stats :
 [![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=developerhasanak)](https://github.com/anuraghazra/github-readme-stats)

  
  [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=developerhasanak&layout=compact&theme=vision-friendly-dark)](https://github.com/anuraghazra/github-readme-stats)

### :hammer_and_wrench: Languages and Tools :
<img src ="https://github.com/devicons/devicon/blob/master/icons/android/android-original.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/kotlin/kotlin-original.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/java/java-original.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/linux/linux-original.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/debian/debian-original-wordmark.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/bash/bash-original.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/git/git-original.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/github/github-original.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/sqlite/sqlite-original.svg" width="40" height="40"/>&nbsp;
<img src ="https://github.com/devicons/devicon/blob/master/icons/firebase/firebase-plain.svg" width="40" height="40"/>&nbsp;
