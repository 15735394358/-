class Add:Calculate
    {
        public override void suan(int a, int b)
        {
            int c = a + b;
            Console.WriteLine("两数相加的和是{0}",a+b);
        }
        public void add(String s1, String s2)
        {
            String d = s1 + s2;
            Console.WriteLine("进行加法运算的结果是{0}",d);
        }
    }
    
    
    
     class Reduce:Calculate
    {
        public override void suan(int a, int b)
        {
            int c = a - b;
            Console.WriteLine("两数相减的差是{0}",c);
        }
        public void reduce(String s1, String s2)
        {
            bool isexist = s1.Contains(s2);
            string s3;
            if (isexist)
            {
                int i = s1.IndexOf(s2);
                s3 = s1.Remove(i, s2.Length);
                reduce(s3, s2);
                if (!s3.Contains(s2))
                {
                    Console.WriteLine("进行减法运算的结果" + s3.ToString());
                }
            }
            else
            {
                Console.WriteLine("无法进行减法运算");
            }
        }
    }
