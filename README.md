# Vigenere-Cipher
#MATLAB Code for Vigenere Cipher Encryption

#defining vigenere function
function cipher_text= vigenere(p_text,key)
p_lower=lower(p_text);
k_lower=lower(key);
p=char(p_lower);
k=char(k_lower);
p=p(find(~isspace(p)));
k=k(find(~isspace(k)));
k1=k;
while(length(k1)<length(p))
    k1=strcat(k1,k);
end
k2=k1(1:length(p));
c=zeros(1,length(p));
for i=1:length(c)
    c(i)= double(p(i))+double(k2(i))-194;
end
c1=mod(c,26)+97;
cipher_text=upper(char(c1));
end

#calling the vigenere cipher function
vigenere('MEET ME LATER','LEMON');




