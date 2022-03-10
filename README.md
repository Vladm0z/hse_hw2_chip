# hse_hw2_chip

[Colab](https://colab.research.google.com/drive/1giruHuC5xG3CJIIF0WeogbgDk31GB0jG?usp=sharing)

Для исследования была выбрана клеточная линия A549 и гистоновая метка H3K4me1.

## Анализ FastQC

HTML-выдача FastQC лежит в data

1-ая ChipSeq реплика | 2-ая ChipSeq реплика | Контроль
--- | --- | ---
[ENCFF052DPD](https://github.com/Vladm0z/hse_hw2_chip/blob/main/data/ENCFF052DPD_fastqc.html) | [ENCFF612KDN](https://github.com/Vladm0z/hse_hw2_chip/blob/main/data/ENCFF612KDN_fastqc.html) | [ENCFF726ZWD](https://github.com/Vladm0z/hse_hw2_chip/blob/main/data/ENCFF726ZWD_fastqc.html)

### FastQC

ENCFF052DPD | ENCFF612KDN | ENCFF726ZWD
--- | --- | ---
![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/ChipSeq_ENCFF052DPD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/ChipSeq_ENCFF726ZWD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/ChipSeq_ENCFF612KDN.png)
![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Pbsq_ENCFF052DPD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Pbsq_ENCFF726ZWD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Pbsq_ENCFF612KDN.png)
![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Psqs_ENCFF052DPD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Psqs_ENCFF726ZWD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Psqs_ENCFF612KDN.png)
![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Pbsc_ENCFF052DPD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Pbsc_ENCFF726ZWD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Pbsc_ENCFF612KDN.png)
![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/PsGCc_ENCFF052DPD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/PsGCc_ENCFF726ZWD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/PsGCc_ENCFF612KDN.png)
![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/PbNc_ENCFF052DPD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/PbNc_ENCFF726ZWD.png) | ![image](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/PbNc_ENCFF612KDN.png)

Подрезание не требуется, качество ридов хорошее.


## Таблица со статистикой по выравниванию на 16 хромосому

|index|Общее число ридов|Выровнившиеся уникально|(%)|Выровнившиеся неуникально|(%)|Не выровнившиеся|(%)|
|ENCFF052DPD|30927779|1438430|4.65%|3792969|12.26%|25696380|83.09%|
|ENCFF726ZWD|30504189|1480427|4.85%|3325623|10.90%|25698139|84.24%|
|ENCFF612KDN|20663767|995771|4.82%|2461697|11.91%|17206299|83.27%|


## Диаграммы Эйлера-Венна

### Пересечение пиков 1 реплики с пиками ENCODE

![Intervene_venn_(1) page-0001](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Intervene_venn_1.png)

### Пересечение пиков ENCODE с пиками 1 реплики

![Intervene_venn (2)_page-0001](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Intervene_venn_2.png)

### Пересечение пиков 2 реплики с пиками ENCODE

![Intervene_venn (3)_page-0001](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Intervene_venn_3.png)

### Пересечение пиков ENCODE с пиками 2 реплики

![Intervene_venn (4)_page-0001](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/Intervene_venn_4.png)


Пересечений получилось мало, так как пиков получилось мало в связи с выравниванием только на одну хромосому. В базе данных ENCODE пики составлены для всех хромосом, поэтому их намного больше. Пересечение наших пиков с ENCODE и пересечение ENCODE с нашими пиками - это не одно и то же: пересечение устроено таким образом, что считается число участков в первом файле таких, что они имеются во втором, аналогично при другом порядке - участки второго, которые имеются в первом.


## Бонусная часть heatmap для bam файлов и соотвествующих им .bigWig файлов

![ENCFF040HPO](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/result.png)
![ENCFF160YWB](https://github.com/Vladm0z/hse_hw2_chip/raw/main/data/result2.png)


