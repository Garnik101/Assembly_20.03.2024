# academy_asm

Problem 2:
                                
Ծրագիրը հրավիրում է օգտվողին մուտքագրել դրական n թիվ, ապա գումարում 0-ից տվյալ թվի միջև ընկած միջակայքի թվերի գումարը (մուտքագրված թիվը ներառյալ) և տպում այն։

• Տող 1-ում Հայտարաված են արտաքին ֆունկցիաներ։

• section .bss-ում հայտարարված է 4 բայթ տարածք՝ double word տիպի n չսկզբնարժեքավորված փոփոխականի համար։

• section .data-ում հայտարարված են ֆունկցիաների համար անհրաժեշտ format string-երը։

• section .text-ի 11-23 տողերի սկզբում ներկայացված է function prologue-ը, որից հետո՝ User Input-ը՝ n փոփոխականի համար։ Վերջում rbx ռեգիստրը, որը ծառայում է որպես loop1 ցիկլի արժեքների գումարի պահման փոփխական, զրոյացվում է, ապա որպես ցիկլի counter-ռեգիստրի (rcx) արժեք, այս ռեգստրի մեջ տեղափոխվում է n փոփոխականի հասցեում գտնվող արժեքը։

• 24-26 տողերում ներկայացված է loop1 ցիկլը, որի յուրաքանչյուր իտերացիայի ընթացքում rcx-ի արժեքը գումարվում է rbx֊ին, ապա rcx-ի արժեքը 1-ով նվազում է և այս գործողություններւ կրկնվում են քանի դեռ rcx ռեգիստրի արժեքը հավասար չէ 0-ի։ Երբ այն պայմանն ապահովվում՝ անցում է կատարվում ծրագրի հաջորդ ինստրուկցիային։
    
 • 28-34 տողերում փոխանցվում են printf ֆունկցիայի անհրաժեշտ արգումենտները և տպվում է rbx-ի արժեքը (գումարան արդյունքը), ապա ներկայացված է function epilogue-ը և ծրագրի ավարտը։
