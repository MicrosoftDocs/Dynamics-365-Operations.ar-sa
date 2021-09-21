---
title: لا يتم حساب أسعار الوحدات على أوامر الشراء استنادًا إلى تحويل الوحدة
description: لا يتم حساب أسعار الوحدات على أوامر الشراء استنادًا إلى تحويل الوحدة
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475467"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>لا يتم حساب أسعار الوحدات على أوامر الشراء استنادًا إلى تحويل الوحدة

## <a name="symptoms"></a>العلامات

عند تغيير وحدة في أمر شراء، لا يُعاد حساب أسعار الاتفاقيات التجارية وفقًا لتعريفات تحويل الوحدة.

## <a name="cause"></a>السبب

يتم الحصول على الأسعار دائمًا من الاتفاقيات التجارية (أو إعدادات السعر الأخرى في النظام، مثل اتفاقيات البيع أو أسعار الأصناف)، ويتم تعيينها لوحدة.

إذا تغيّرت الوحدة على بند الأمر، فسيبحث النظام عن سعر للوحدة الجديدة ويطبق هذا السعر. في حالة عدم العثور على سعر للوحدة، فلن يطبّق النظام أي سعر. لا يمكن استخدام تحويل الوحدة لإعادة حساب السعر في وحدة أخرى. نظريًا، قد لا يساوي السعر لصندوق واحد من عشرة صناديق عشر مرات السعر الخاص بصندوق واحد.

## <a name="workaround"></a>حل بديل

هناك طريقة لحل هذه المشكلة وهي التأكد من وجود اتفاقيات تجارية للوحدات التي تتوقع استخدامها في بنود الأوامر الخاصة بالصنف.
