<h1>Thai Supreme Court Cases (TSCC) Dataset</h1>
<p>
This is the dataset first appeared in the paper "Predicting Judicial Decisions of Criminal Cases from Thai Supreme Court Using Bi-directional GRU with Attention Mechanism" which will be presented at the 5th Asian Conference on Defense Technology (ACDT 2018) in Hanoi, Vietnam.
</p>
<p>
TSCC comes from 1,000 criminal judgements from the Supreme Court Judgement Search System created by the Supreme Court of Thailand [1]. These judgements were judged since 1958 (B.E. 2501) using Thai Criminal Code B.E. 2499 (1956) [2]. Those judgements could be classified as three categories:
<ul>
<li>The offence against Life and Body like Murder, Manslaughter and Assault.</li>
<li>The offence against Property such as Theft, Fraud and Misappropriation.</li>
<li>The offence against Fame which is Defamation and Insult.</li>
</ul>
</p>
<p>
TSCC consists of two tables, Judgement and Law. Judgement table consists of 1,207 issues extracted from aforementioned judgements by the firmly effort of our expert. While Law composed of 122 legal provisions from 76 sections in Thai Criminal Code. We provide the .csv version which is suitable for model training and the Excel (.xlsx) version which is proper for analyzing data characteristics.
</p>
<h1>Disclaimer</h1>
<p>
Please note that TSCC dataset is created <strong>for the academic purpose.</strong> Therefore, please <strong>do not</strong> use this for commercial.
</p>
<h1>The Example of Correct/Incorrect Prediction of Our Proposed Model</h1>
<p><strong>Our model's inputs are text of Fact and Law in Thai.</strong> However, we provide the English translation for every Thai text in parentheses. Besides, all translation of Law text comes from [3].</p>
<h2>Correct</h2>
<p>
<strong>Fact:</strong> การที่จำเลยไปหยิบอาวุธปืนจากรถยนต์มาเพื่อป้องกันบุตรของตน และเหตุที่กระสุนปืนลั่นเกิดจากการแย่งอาวุธปืนระหว่างจำเลยกับโจทก์ร่วม
 อันสืบเนื่องมาจากจำเลยใช้อาวุธปืนเพื่อป้องกันบุตรของตนดังกล่าว (The defendant picked up the firearms from his car to protect his child. The reason that the gun was fired comes from the struggle between the defendant and the co-plaintiff due to the defendant used his firearms to protect his child.)
</p>
<p>  
<strong>Law:</strong> ผู้ใดกระทำโดยประมาท และการกระทำนั้นเป็นเหตุให้ผู้อื่นรับอันตรายสาหัส ต้องระวางโทษจำคุกไม่เกินสามปี หรือปรับไม่เกินหกพันบาท หรือ
ทั้งจำทั้งปรับ กระทำโดยประมาท ได้แก่กระทำความผิดมิใช่โดยเจตนา แต่กระทำโดยปราศจากความระมัดระวังซึ่งบุคคลในภาวะเช่นนั้นจักต้องมีตามวิสัยและพฤติการณ์ และผู้กระทำอาจใช้ความระมัดระวังเช่นว่านั้นได้ แต่หาได้ใช้ให้เพียงพอไม่ ผู้ใดจำต้องกระทำการใดเพื่อป้องกันสิทธิของตนหรือของผู้อื่นให้พ้นภยันตรายซึ่งเกิดจากการประทุษร้ายอันละเมิดต่อกฎหมาย และเป็นภยันตรายที่ใกล้จะถึง ถ้าได้กระทำพอสมควรแก่เหตุ การกระทำนั้นเป็นการป้องกันโดยชอบด้วยกฎหมาย ผู้นั้นไม่มีความผิด (Whoever, committing the act by negligence and such act to cause the grievous bodily harm to the other person, shall be imprisoned three years or fined not more of six thousand Baht, or both. To commit an act by negligence is to commit an offence unintentionally but without exercising such care as might be expected from a person under such condition and circumstances, and the doer could exercise such care but did not do so sufficiently. Whoever commits any act for the defense of his own right or other person's right in order to except from a danger arising out of violence tortuous to the law and such danger to be imminent, if reasonably having committed under the circumstance, such act is a lawful defense, and such person shall not have a guilt.)
</p>
<p>
<strong>Model's Output and Correct Answer:</strong> 0 (The defendant is not guilty of Bodily Harm as a Result of Negligence.)
</p>
<h2>Incorrect</h2>
<p>
<strong>Fact:</strong> จำเลยเป็นคนนำรถเกรดถนนของ ส. ที่ฝากไว้แก่ผู้เสียหายไปจากความครอบครองของผู้เสียหาย ตามที่ผู้เสียหายแจ้งให้จำเลยเคลื่อนย้ายไปจากปั้มแก๊สของผู้เสียหาย เป็นกรณีที่ผู้เสียหายซึ่งเป็นผู้มีสิทธิครอบครองทรัพย์ส่งมอบการครอบครองให้แก่จำเลยด้วยความสมัครใจ (The defendant brought the road grader of S. which was deposited to the victim from his possession as he informed the defendant to move that grader from his gas station. This case could be implied that the defendant who has the legal possession of the property handed over that to the defendant voluntarily.)
</p>
<p>
<strong>Law:</strong>  ผู้ใดเอาทรัพย์ของผู้อื่น หรือที่ผู้อื่นเป็นเจ้าของรวมอยู่ด้วยไปโดยทุจริต ผู้นั้นกระทำความผิดฐานลักทรัพย์ ต้องระวางโทษจำคุกไม่เกินสามปี และปรับไม่เกินหกพันบาท (Whoever dishonestly takes away any property of another person or which the other person to be co-owner to be said to commit the theft, shall be imprisoned not out of three years and fined not more of six thousand Baht.)
</p>
<p>
<strong>Model's Output but Wrong:</strong> 1 (The defendant is guilty of theft.)
</p>
<h1>References</h1>
<p>[1]	Information Technology and Communication Center in Thai Supreme Court. Thai Supreme Court Judgement Search System [Online]. Available: <a href="http://deka.supremecourt.or.th/"  target="_blank">http://deka.supremecourt.or.th/</a></p>
<p>[2]	Office of the Council of State. “Thai Criminal Code” [Online]. Available: <a href="http://web.krisdika.go.th/data/law/law4/%bb06/%bb06-20-9999-update.pdf" target="_blank" rel="no">http://web.krisdika.go.th/data/law/law4/%bb06/%bb06-20-9999-update.pdf</a></p>
<p>[3]	“Thai  Criminal  Code”, library.siam-legal.com. [Online].  Available:  <a href="http://library.siam-legal.com/thai-criminal-code/" target="_blank">http://library.siam-legal.com/thai-criminal-code/</a>.  [Accessed:  25-AUG-2017]</p>
