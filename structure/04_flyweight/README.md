# 享元模式

享元模式是细粒度控制主体构成的一种方式，英文叫 flyweight，单词分开看反倒更容易理解，fly-weight,看起来是要消减对象的大小/重量(size/weight),对！就是这个意思!抽取对象中的不变部分，使其能够容易的被复用或者共用，进而能够减小内存占用，优化性能，提高运行时效率，比如，会减少对象在内存分配/克隆时的空间大小，减小对象内存占用损耗，缩短响应时间等。

注意：实际上完整的享元模式，包含两部分可以被共享的部分，不可以被共享部分，两者组合起来才构成一个完整的整体，设计享元模式，严谨的讲需要针对可共享部分与不可共享两部分设计接口。


单纯享元模式：在单纯享元模式中，所有的具体享元类都是可以共享的，不存在非共享具体享元类。
复合享元模式：将一些单纯享元对象使用组合模式加以组合，还可以形成复合享元对象，这样的复合享元对象本身不能共享，但是它们可以分解成单纯享元对象，而后者则可以共享。

享元的的可共享部分在程序是设计，一般是集中管理的，一般设计为一个存储map的，享元的不可共享部分，一般是即用即创建，完全的专有模式.

现实生活中的快递送货任务就一个很好的享元模式，快递公司的快递员是共享的，并且可以重复使用，快递公司不可能送一个快递雇一个快递员，否则，这个代价太大巨大了，但是快递员送的包裹是不一样，这是每个人的私有物品，所以不变的快递员+一直在变化的快递，才能构成一次完整的送货任务。





