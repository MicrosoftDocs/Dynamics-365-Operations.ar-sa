---
title: إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى رسائل البريد الكتروني للمعاملات والإيصالات
description: يوضح هذا المقال كيفية إدراج رموز QR والرموز الشريطية التي تمثل معرفات الأوامر في رسائل البريد الإلكتروني للحركات والإيصالات في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 2832d1df3893e124759e4719a64341494cea2204
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272034"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى رسائل البريد الكتروني للمعاملات والإيصالات

[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية إدراج رموز QR والرموز الشريطية التي تمثل معرفات الأوامر في رسائل البريد الإلكتروني للحركات والإيصالات في Microsoft Dynamics 365 Commerce.

يمكنك بسهولة تضمين رموز QR والرموز الشريطية في رسائل البريد الكتروني للمعاملات للمساعدة في تسريع عملية البحث عن الأوامر في بيئة بيع بالتجزئة. لادراج رموز QR والرموز الشريطية في رسائل البريد الكتروني، استخدم علامة **\<img\>** من HTML التي تتطلب صورة رمز QR أو رمز شريطي من خدمة الإنشاء والعرض. لا توفر Microsoft هذه الخدمة. ومع ذلك، يوجد العديد من الخدمات المجانية أو غير المكلفة التي يمكنها تقديم رموز QR أو الرموز الشريطية التي يتم إنشاؤها ديناميكيًا بناء على القيمة التي يتم تمريرها في سلسلة الاستعلام.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى رسالة بريد إلكتروني للمعاملات

لادراج رمز استجابة سريعة (QR) أو رمز شريطي في بريد إلكتروني للمعاملات يتم إرساله كجزء من عملية شراء ضمن التجارة الإلكترونية، اتبع الخطوات التالية.

1. افتح HTML المصدر الخاص بقالب البريد الإلكتروني للمعاملات، وأضف علامة **\<img\>** من HTML التي تشير إلى خدمة رمز QR أو الرمز الشريطي. فيما يلي مثال على ذلك.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    فيما يلي شرح للمثال السابق:

    - يمثل **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** مجال خدمة رمز QR أو الرمز الشريطي.
    - تمثل **البيانات** المعلمة التي تستخدمها خدمة رمز QR أو الرمز الشريطي لاستلام المحتوى الذي يجب عرضه كرمز QR أو كرمز شريطي.

        يجب تعيين القيمة **%salesid%** إلى هذه المعلمة. في هذا المثال، لاحظ أنه يتم استخدام القيمة أيضًا كنص بديل للصورة.

    - يمثل **param1** و **param2** معلمات اختيارية إضافية.

1. انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة**، ثم قم بتحميل HTML المحدّث إلى قالب البريد الكتروني الخاص بالحركات المناسب.

> [!NOTE]
> قد تختلف المعلمات فيما بين موفري خدمة رمز QR والرمز الشريطي. لذلك، تأكد من الاتصال بموفر الخدمة لتأكيد المعلمات التي يجب تعيين القيم لها.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى رسالة بريد إلكتروني للإيصال 

لإدراج رمز استجابة سريعة (QR) أو رمز شريطي في رسالة بريد إلكتروني للإيصال يمكن إرسالها بعد إجراء عملية شراء في نقطة البيع (POS)، اتبع الخطوات التالية.

1. فتح HTML المصدر الخاص بقالب البريد الإلكتروني للإيصال، وأضف علامة **\<img\>** من HTML التي تشير إلى خدمة رمز QR أو الرمز الشريطي. وفيما يلي مثال على ذلك.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    فيما يلي شرح للمثال السابق:

    - يمثل **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** مجال خدمة رمز QR أو الرمز الشريطي.
    - تمثل **البيانات** المعلمة التي تستخدمها خدمة رمز QR أو الرمز الشريطي لاستلام المحتوى الذي يجب عرضه كرمز QR أو كرمز شريطي.

        يجب تعيين القيمة **%receiptid%** إلى هذه المعلمة. في هذا المثال، لاحظ أنه يتم استخدام القيمة أيضًا كنص بديل للصورة.

    - يمثل **param1** و **param2** معلمات اختيارية إضافية.

1. انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة**، ثم قم بتحميل HTML المحدّث إلى قالب البريد الكتروني الذي يتضمن معرف البريد الإلكتروني **emailrecpt**.

> [!NOTE]
> قد تختلف المعلمات فيما بين موفري خدمة رمز QR والرمز الشريطي. لذلك، تأكد من الاتصال بموفر الخدمة لتأكيد المعلمات التي يجب تعيين القيم لها.

## <a name="additional-resources"></a>الموارد الإضافية

[إرسال إيصالات الاستلام عبر البريد الإلكتروني من نقطة البيع الحديثة](email-receipts.md)

[إنشاء قوالب بريد إلكتروني لأحداث المعاملات](email-templates-transactions.md)
