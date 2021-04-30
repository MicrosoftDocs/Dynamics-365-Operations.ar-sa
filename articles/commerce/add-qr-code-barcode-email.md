---
title: إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى رسائل البريد الكتروني للمعاملات والإيصالات
description: يوضح هذا الموضوع كيفية إدراج رموز QR والرموز الشريطية التي تمثل معرفات الأوامر في رسائل البريد الإلكتروني للحركات والإيصالات في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 791b244c867ea4263f08250abf220a1b75784cad
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907853"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="3dfe2-103">إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى رسائل البريد الكتروني للمعاملات والإيصالات</span><span class="sxs-lookup"><span data-stu-id="3dfe2-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3dfe2-104">يوضح هذا الموضوع كيفية إدراج رموز QR والرموز الشريطية التي تمثل معرفات الأوامر في رسائل البريد الإلكتروني للحركات والإيصالات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3dfe2-105">يمكنك بسهولة تضمين رموز QR والرموز الشريطية في رسائل البريد الكتروني للمعاملات للمساعدة في تسريع عملية البحث عن الأوامر في بيئة بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="3dfe2-106">لادراج رموز QR والرموز الشريطية في رسائل البريد الكتروني، استخدم علامة **\<img\>** من HTML التي تتطلب صورة رمز QR أو رمز شريطي من خدمة الإنشاء والعرض.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="3dfe2-107">لا توفر Microsoft هذه الخدمة.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="3dfe2-108">ومع ذلك، يوجد العديد من الخدمات المجانية أو غير المكلفة التي يمكنها تقديم رموز QR أو الرموز الشريطية التي يتم إنشاؤها ديناميكيًا بناء على القيمة التي يتم تمريرها في سلسلة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="3dfe2-109">إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى رسالة بريد إلكتروني للمعاملات</span><span class="sxs-lookup"><span data-stu-id="3dfe2-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="3dfe2-110">لادراج رمز استجابة سريعة (QR) أو رمز شريطي في بريد إلكتروني للمعاملات يتم إرساله كجزء من عملية شراء ضمن التجارة الإلكترونية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="3dfe2-111">افتح HTML المصدر الخاص بقالب البريد الإلكتروني للمعاملات، وأضف علامة **\<img\>** من HTML التي تشير إلى خدمة رمز QR أو الرمز الشريطي.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="3dfe2-112">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="3dfe2-113">فيما يلي شرح للمثال السابق:</span><span class="sxs-lookup"><span data-stu-id="3dfe2-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="3dfe2-114">يمثل **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** مجال خدمة رمز QR أو الرمز الشريطي.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="3dfe2-115">تمثل **البيانات** المعلمة التي تستخدمها خدمة رمز QR أو الرمز الشريطي لاستلام المحتوى الذي يجب عرضه كرمز QR أو كرمز شريطي.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="3dfe2-116">يجب تعيين القيمة **%salesid%** إلى هذه المعلمة.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="3dfe2-117">في هذا المثال، لاحظ أنه يتم استخدام القيمة أيضًا كنص بديل للصورة.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="3dfe2-118">يمثل **param1** و **param2** معلمات اختيارية إضافية.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="3dfe2-119">انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة**، ثم قم بتحميل HTML المحدّث إلى قالب البريد الكتروني الخاص بالحركات المناسب.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="3dfe2-120">قد تختلف المعلمات فيما بين موفري خدمة رمز QR والرمز الشريطي.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="3dfe2-121">لذلك، تأكد من الاتصال بموفر الخدمة لتأكيد المعلمات التي يجب تعيين القيم لها.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="3dfe2-122">إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى رسالة بريد إلكتروني للإيصال</span><span class="sxs-lookup"><span data-stu-id="3dfe2-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="3dfe2-123">لإدراج رمز استجابة سريعة (QR) أو رمز شريطي في رسالة بريد إلكتروني للإيصال يمكن إرسالها بعد إجراء عملية شراء في نقطة البيع (POS)، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="3dfe2-124">فتح HTML المصدر الخاص بقالب البريد الإلكتروني للإيصال، وأضف علامة **\<img\>** من HTML التي تشير إلى خدمة رمز QR أو الرمز الشريطي.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="3dfe2-125">وفيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="3dfe2-126">فيما يلي شرح للمثال السابق:</span><span class="sxs-lookup"><span data-stu-id="3dfe2-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="3dfe2-127">يمثل **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** مجال خدمة رمز QR أو الرمز الشريطي.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="3dfe2-128">تمثل **البيانات** المعلمة التي تستخدمها خدمة رمز QR أو الرمز الشريطي لاستلام المحتوى الذي يجب عرضه كرمز QR أو كرمز شريطي.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="3dfe2-129">يجب تعيين القيمة **%receiptid%** إلى هذه المعلمة.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="3dfe2-130">في هذا المثال، لاحظ أنه يتم استخدام القيمة أيضًا كنص بديل للصورة.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="3dfe2-131">يمثل **param1** و **param2** معلمات اختيارية إضافية.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="3dfe2-132">انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة**، ثم قم بتحميل HTML المحدّث إلى قالب البريد الكتروني الذي يتضمن معرف البريد الإلكتروني **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="3dfe2-133">قد تختلف المعلمات فيما بين موفري خدمة رمز QR والرمز الشريطي.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="3dfe2-134">لذلك، تأكد من الاتصال بموفر الخدمة لتأكيد المعلمات التي يجب تعيين القيم لها.</span><span class="sxs-lookup"><span data-stu-id="3dfe2-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3dfe2-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3dfe2-135">Additional resources</span></span>

[<span data-ttu-id="3dfe2-136">إرسال إيصالات الاستلام عبر البريد الإلكتروني من نقطة البيع الحديثة</span><span class="sxs-lookup"><span data-stu-id="3dfe2-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="3dfe2-137">إنشاء قوالب بريد إلكتروني لأحداث المعاملات</span><span class="sxs-lookup"><span data-stu-id="3dfe2-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
